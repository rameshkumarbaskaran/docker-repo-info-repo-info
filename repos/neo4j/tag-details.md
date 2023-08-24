<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.25`](#neo4j4425)
-	[`neo4j:4.4.25-community`](#neo4j4425-community)
-	[`neo4j:4.4.25-enterprise`](#neo4j4425-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.11`](#neo4j511)
-	[`neo4j:5.11-bullseye`](#neo4j511-bullseye)
-	[`neo4j:5.11-community`](#neo4j511-community)
-	[`neo4j:5.11-community-bullseye`](#neo4j511-community-bullseye)
-	[`neo4j:5.11-community-ubi8`](#neo4j511-community-ubi8)
-	[`neo4j:5.11-enterprise`](#neo4j511-enterprise)
-	[`neo4j:5.11-enterprise-bullseye`](#neo4j511-enterprise-bullseye)
-	[`neo4j:5.11-enterprise-ubi8`](#neo4j511-enterprise-ubi8)
-	[`neo4j:5.11-ubi8`](#neo4j511-ubi8)
-	[`neo4j:5.11.0`](#neo4j5110)
-	[`neo4j:5.11.0-bullseye`](#neo4j5110-bullseye)
-	[`neo4j:5.11.0-community`](#neo4j5110-community)
-	[`neo4j:5.11.0-community-bullseye`](#neo4j5110-community-bullseye)
-	[`neo4j:5.11.0-community-ubi8`](#neo4j5110-community-ubi8)
-	[`neo4j:5.11.0-enterprise`](#neo4j5110-enterprise)
-	[`neo4j:5.11.0-enterprise-bullseye`](#neo4j5110-enterprise-bullseye)
-	[`neo4j:5.11.0-enterprise-ubi8`](#neo4j5110-enterprise-ubi8)
-	[`neo4j:5.11.0-ubi8`](#neo4j5110-ubi8)
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
$ docker pull neo4j@sha256:15d6cf2eee2f62d777104f4681aeab8d520e8bd235d11679539ed34a02a08de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:1885c7a57d7ee7e82010f39ac03ee211300909b0e0644f2db57c204684d71204
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298588916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18691e2a7b3295dc49268bf41c57556a3a024c2950e30d9d681b99c14bcd3ac5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:02:38 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Thu, 24 Aug 2023 20:20:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=44d8e1c6af11199478ab8d2be399f8dc7ff819d23ef9983d70b15ae7d9918e26 NEO4J_TARBALL=neo4j-community-4.4.25-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 20:20:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 20:20:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 20:20:05 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 20:20:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 20:20:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 20:20:18 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 20:20:18 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 20:20:18 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 20:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 20:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f416efba54d09e37495a54336ac55d40fc467f753f97e78f060748b4513e5`  
		Last Modified: Wed, 16 Aug 2023 17:06:20 GMT  
		Size: 144.8 MB (144831672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c62682f667d09a0cca46fc085b81d88f257a510a439faa87f70ffe2ad56af9e`  
		Last Modified: Thu, 24 Aug 2023 20:21:10 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a0c02739494860d05e25e344675b0031c80cb90db4e270e289bc8fb7ad368f`  
		Last Modified: Thu, 24 Aug 2023 20:21:10 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2996ae61db01df3920a8175b2440375e0de17a06fa17c46cd6c8d2ee283a3323`  
		Last Modified: Thu, 24 Aug 2023 20:21:18 GMT  
		Size: 122.3 MB (122326419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a2fba937626be5d6fddc8e3703b9baefbec84a97b621c805c03946a23c28017b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293860751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4918a3e14bf43089f40588439222f65de812e6291e4ba2aa223cd0897171cc0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:22:18 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Thu, 24 Aug 2023 19:39:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=44d8e1c6af11199478ab8d2be399f8dc7ff819d23ef9983d70b15ae7d9918e26 NEO4J_TARBALL=neo4j-community-4.4.25-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 19:39:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 19:39:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 19:39:52 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 19:40:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 19:40:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 19:40:08 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 19:40:08 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 19:40:08 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 19:40:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 19:40:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e09cb30a1ef0915a1ffb7a7e09dbfbbd6ca50b0de70ef22c1ecb37d83b229`  
		Last Modified: Wed, 16 Aug 2023 17:31:53 GMT  
		Size: 141.6 MB (141565229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059e80faeba713a27f4eeec79e5365138e97d944d4fd8e8a60b8321d121cead1`  
		Last Modified: Thu, 24 Aug 2023 19:40:57 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d587d9283f8c431a5f8dae1a6b26ff7851ea1754b5bb812ca51795f70d12e8`  
		Last Modified: Thu, 24 Aug 2023 19:40:57 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e179dcd6bba8607aecee468aadba835ba7d73aad8efeb11e13d5ae0985de8d6`  
		Last Modified: Thu, 24 Aug 2023 19:41:06 GMT  
		Size: 122.2 MB (122219532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:15d6cf2eee2f62d777104f4681aeab8d520e8bd235d11679539ed34a02a08de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1885c7a57d7ee7e82010f39ac03ee211300909b0e0644f2db57c204684d71204
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298588916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18691e2a7b3295dc49268bf41c57556a3a024c2950e30d9d681b99c14bcd3ac5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:02:38 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Thu, 24 Aug 2023 20:20:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=44d8e1c6af11199478ab8d2be399f8dc7ff819d23ef9983d70b15ae7d9918e26 NEO4J_TARBALL=neo4j-community-4.4.25-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 20:20:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 20:20:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 20:20:05 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 20:20:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 20:20:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 20:20:18 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 20:20:18 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 20:20:18 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 20:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 20:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f416efba54d09e37495a54336ac55d40fc467f753f97e78f060748b4513e5`  
		Last Modified: Wed, 16 Aug 2023 17:06:20 GMT  
		Size: 144.8 MB (144831672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c62682f667d09a0cca46fc085b81d88f257a510a439faa87f70ffe2ad56af9e`  
		Last Modified: Thu, 24 Aug 2023 20:21:10 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a0c02739494860d05e25e344675b0031c80cb90db4e270e289bc8fb7ad368f`  
		Last Modified: Thu, 24 Aug 2023 20:21:10 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2996ae61db01df3920a8175b2440375e0de17a06fa17c46cd6c8d2ee283a3323`  
		Last Modified: Thu, 24 Aug 2023 20:21:18 GMT  
		Size: 122.3 MB (122326419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a2fba937626be5d6fddc8e3703b9baefbec84a97b621c805c03946a23c28017b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293860751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4918a3e14bf43089f40588439222f65de812e6291e4ba2aa223cd0897171cc0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:22:18 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Thu, 24 Aug 2023 19:39:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=44d8e1c6af11199478ab8d2be399f8dc7ff819d23ef9983d70b15ae7d9918e26 NEO4J_TARBALL=neo4j-community-4.4.25-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 19:39:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 19:39:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 19:39:52 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 19:40:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 19:40:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 19:40:08 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 19:40:08 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 19:40:08 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 19:40:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 19:40:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e09cb30a1ef0915a1ffb7a7e09dbfbbd6ca50b0de70ef22c1ecb37d83b229`  
		Last Modified: Wed, 16 Aug 2023 17:31:53 GMT  
		Size: 141.6 MB (141565229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059e80faeba713a27f4eeec79e5365138e97d944d4fd8e8a60b8321d121cead1`  
		Last Modified: Thu, 24 Aug 2023 19:40:57 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d587d9283f8c431a5f8dae1a6b26ff7851ea1754b5bb812ca51795f70d12e8`  
		Last Modified: Thu, 24 Aug 2023 19:40:57 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e179dcd6bba8607aecee468aadba835ba7d73aad8efeb11e13d5ae0985de8d6`  
		Last Modified: Thu, 24 Aug 2023 19:41:06 GMT  
		Size: 122.2 MB (122219532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:c79099a26cff90ea7b7d00dee35cd799d3945fb50083c3c2c30403d7215934db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:85472e314fed6663be33ea7ea09b15529e3532beb1355918dab9bf4f95420e9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398474879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dcdb98b4ea2746e3e070d2fe06093d38a6cc5cae72d90a0b41ff590f20d101`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:02:38 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Thu, 24 Aug 2023 20:20:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c63ccf85c310be093cf030c85618555d75f06fce80239a1a618bd343f5c894aa NEO4J_TARBALL=neo4j-enterprise-4.4.25-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 20:20:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 20:20:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 20:20:22 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 20:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 20:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 20:20:37 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 20:20:37 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 20:20:37 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 20:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 20:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f416efba54d09e37495a54336ac55d40fc467f753f97e78f060748b4513e5`  
		Last Modified: Wed, 16 Aug 2023 17:06:20 GMT  
		Size: 144.8 MB (144831672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb8c3ab4cba32d406feffa692c8fe5292cf5dede417b57123429fbc211316ef`  
		Last Modified: Thu, 24 Aug 2023 20:21:31 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd975b300d70f6a4021d6e1c16f858c2b152b018800fc01cc1ebde830fc2cf0`  
		Last Modified: Thu, 24 Aug 2023 20:21:31 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d9dcf794bd070d0790c41afc31234b9b1c7a0e90d22cd25ea2d6a5222e2eb`  
		Last Modified: Thu, 24 Aug 2023 20:21:42 GMT  
		Size: 222.2 MB (222212382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:78d329426bab54bb843c2d5f67766d278a17ded93d16ce72f583a89996a20853
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393747157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52944a76587c514afbe2318472d2c7b2bf751eaddea782d9abede6603c4e15e7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:22:18 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Thu, 24 Aug 2023 19:40:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c63ccf85c310be093cf030c85618555d75f06fce80239a1a618bd343f5c894aa NEO4J_TARBALL=neo4j-enterprise-4.4.25-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 19:40:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 19:40:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 19:40:12 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 19:40:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 19:40:26 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 19:40:26 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 19:40:26 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 19:40:26 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 19:40:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 19:40:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e09cb30a1ef0915a1ffb7a7e09dbfbbd6ca50b0de70ef22c1ecb37d83b229`  
		Last Modified: Wed, 16 Aug 2023 17:31:53 GMT  
		Size: 141.6 MB (141565229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac9d37a07a4e53120bd763851e062d8978d50803412dea99e178420f0b2d7c8`  
		Last Modified: Thu, 24 Aug 2023 19:41:19 GMT  
		Size: 3.9 KB (3891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c5e167f4405d40075594811b3c3e9fd7aa817f985ff364dee8d38cdb5c9696`  
		Last Modified: Thu, 24 Aug 2023 19:41:19 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d554696f9c31b37a004157ffa4d7563cc64ffffee7735420a860fa0944602280`  
		Last Modified: Thu, 24 Aug 2023 19:41:29 GMT  
		Size: 222.1 MB (222105934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.25`

```console
$ docker pull neo4j@sha256:15d6cf2eee2f62d777104f4681aeab8d520e8bd235d11679539ed34a02a08de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.25` - linux; amd64

```console
$ docker pull neo4j@sha256:1885c7a57d7ee7e82010f39ac03ee211300909b0e0644f2db57c204684d71204
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298588916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18691e2a7b3295dc49268bf41c57556a3a024c2950e30d9d681b99c14bcd3ac5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:02:38 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Thu, 24 Aug 2023 20:20:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=44d8e1c6af11199478ab8d2be399f8dc7ff819d23ef9983d70b15ae7d9918e26 NEO4J_TARBALL=neo4j-community-4.4.25-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 20:20:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 20:20:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 20:20:05 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 20:20:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 20:20:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 20:20:18 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 20:20:18 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 20:20:18 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 20:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 20:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f416efba54d09e37495a54336ac55d40fc467f753f97e78f060748b4513e5`  
		Last Modified: Wed, 16 Aug 2023 17:06:20 GMT  
		Size: 144.8 MB (144831672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c62682f667d09a0cca46fc085b81d88f257a510a439faa87f70ffe2ad56af9e`  
		Last Modified: Thu, 24 Aug 2023 20:21:10 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a0c02739494860d05e25e344675b0031c80cb90db4e270e289bc8fb7ad368f`  
		Last Modified: Thu, 24 Aug 2023 20:21:10 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2996ae61db01df3920a8175b2440375e0de17a06fa17c46cd6c8d2ee283a3323`  
		Last Modified: Thu, 24 Aug 2023 20:21:18 GMT  
		Size: 122.3 MB (122326419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.25` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a2fba937626be5d6fddc8e3703b9baefbec84a97b621c805c03946a23c28017b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293860751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4918a3e14bf43089f40588439222f65de812e6291e4ba2aa223cd0897171cc0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:22:18 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Thu, 24 Aug 2023 19:39:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=44d8e1c6af11199478ab8d2be399f8dc7ff819d23ef9983d70b15ae7d9918e26 NEO4J_TARBALL=neo4j-community-4.4.25-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 19:39:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 19:39:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 19:39:52 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 19:40:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 19:40:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 19:40:08 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 19:40:08 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 19:40:08 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 19:40:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 19:40:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e09cb30a1ef0915a1ffb7a7e09dbfbbd6ca50b0de70ef22c1ecb37d83b229`  
		Last Modified: Wed, 16 Aug 2023 17:31:53 GMT  
		Size: 141.6 MB (141565229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059e80faeba713a27f4eeec79e5365138e97d944d4fd8e8a60b8321d121cead1`  
		Last Modified: Thu, 24 Aug 2023 19:40:57 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d587d9283f8c431a5f8dae1a6b26ff7851ea1754b5bb812ca51795f70d12e8`  
		Last Modified: Thu, 24 Aug 2023 19:40:57 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e179dcd6bba8607aecee468aadba835ba7d73aad8efeb11e13d5ae0985de8d6`  
		Last Modified: Thu, 24 Aug 2023 19:41:06 GMT  
		Size: 122.2 MB (122219532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.25-community`

```console
$ docker pull neo4j@sha256:15d6cf2eee2f62d777104f4681aeab8d520e8bd235d11679539ed34a02a08de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.25-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1885c7a57d7ee7e82010f39ac03ee211300909b0e0644f2db57c204684d71204
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298588916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18691e2a7b3295dc49268bf41c57556a3a024c2950e30d9d681b99c14bcd3ac5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:02:38 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Thu, 24 Aug 2023 20:20:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=44d8e1c6af11199478ab8d2be399f8dc7ff819d23ef9983d70b15ae7d9918e26 NEO4J_TARBALL=neo4j-community-4.4.25-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 20:20:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 20:20:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 20:20:05 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 20:20:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 20:20:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 20:20:18 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 20:20:18 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 20:20:18 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 20:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 20:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f416efba54d09e37495a54336ac55d40fc467f753f97e78f060748b4513e5`  
		Last Modified: Wed, 16 Aug 2023 17:06:20 GMT  
		Size: 144.8 MB (144831672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c62682f667d09a0cca46fc085b81d88f257a510a439faa87f70ffe2ad56af9e`  
		Last Modified: Thu, 24 Aug 2023 20:21:10 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a0c02739494860d05e25e344675b0031c80cb90db4e270e289bc8fb7ad368f`  
		Last Modified: Thu, 24 Aug 2023 20:21:10 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2996ae61db01df3920a8175b2440375e0de17a06fa17c46cd6c8d2ee283a3323`  
		Last Modified: Thu, 24 Aug 2023 20:21:18 GMT  
		Size: 122.3 MB (122326419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.25-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a2fba937626be5d6fddc8e3703b9baefbec84a97b621c805c03946a23c28017b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293860751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4918a3e14bf43089f40588439222f65de812e6291e4ba2aa223cd0897171cc0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:22:18 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Thu, 24 Aug 2023 19:39:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=44d8e1c6af11199478ab8d2be399f8dc7ff819d23ef9983d70b15ae7d9918e26 NEO4J_TARBALL=neo4j-community-4.4.25-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 19:39:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 19:39:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 19:39:52 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 19:40:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 19:40:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 19:40:08 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 19:40:08 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 19:40:08 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 19:40:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 19:40:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e09cb30a1ef0915a1ffb7a7e09dbfbbd6ca50b0de70ef22c1ecb37d83b229`  
		Last Modified: Wed, 16 Aug 2023 17:31:53 GMT  
		Size: 141.6 MB (141565229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059e80faeba713a27f4eeec79e5365138e97d944d4fd8e8a60b8321d121cead1`  
		Last Modified: Thu, 24 Aug 2023 19:40:57 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d587d9283f8c431a5f8dae1a6b26ff7851ea1754b5bb812ca51795f70d12e8`  
		Last Modified: Thu, 24 Aug 2023 19:40:57 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e179dcd6bba8607aecee468aadba835ba7d73aad8efeb11e13d5ae0985de8d6`  
		Last Modified: Thu, 24 Aug 2023 19:41:06 GMT  
		Size: 122.2 MB (122219532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.25-enterprise`

```console
$ docker pull neo4j@sha256:c79099a26cff90ea7b7d00dee35cd799d3945fb50083c3c2c30403d7215934db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.25-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:85472e314fed6663be33ea7ea09b15529e3532beb1355918dab9bf4f95420e9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398474879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dcdb98b4ea2746e3e070d2fe06093d38a6cc5cae72d90a0b41ff590f20d101`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:02:38 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Thu, 24 Aug 2023 20:20:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c63ccf85c310be093cf030c85618555d75f06fce80239a1a618bd343f5c894aa NEO4J_TARBALL=neo4j-enterprise-4.4.25-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 20:20:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 20:20:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 20:20:22 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 20:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 20:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 20:20:37 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 20:20:37 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 20:20:37 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 20:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 20:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f416efba54d09e37495a54336ac55d40fc467f753f97e78f060748b4513e5`  
		Last Modified: Wed, 16 Aug 2023 17:06:20 GMT  
		Size: 144.8 MB (144831672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb8c3ab4cba32d406feffa692c8fe5292cf5dede417b57123429fbc211316ef`  
		Last Modified: Thu, 24 Aug 2023 20:21:31 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd975b300d70f6a4021d6e1c16f858c2b152b018800fc01cc1ebde830fc2cf0`  
		Last Modified: Thu, 24 Aug 2023 20:21:31 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d9dcf794bd070d0790c41afc31234b9b1c7a0e90d22cd25ea2d6a5222e2eb`  
		Last Modified: Thu, 24 Aug 2023 20:21:42 GMT  
		Size: 222.2 MB (222212382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.25-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:78d329426bab54bb843c2d5f67766d278a17ded93d16ce72f583a89996a20853
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393747157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52944a76587c514afbe2318472d2c7b2bf751eaddea782d9abede6603c4e15e7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:22:18 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Thu, 24 Aug 2023 19:40:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c63ccf85c310be093cf030c85618555d75f06fce80239a1a618bd343f5c894aa NEO4J_TARBALL=neo4j-enterprise-4.4.25-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 24 Aug 2023 19:40:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
# Thu, 24 Aug 2023 19:40:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 24 Aug 2023 19:40:12 GMT
COPY multi:b4e555cf4a865db7ac955e204b7d9f288c4ba077e688882dbe94074bda1d191e in /startup/ 
# Thu, 24 Aug 2023 19:40:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.25-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 19:40:26 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 19:40:26 GMT
WORKDIR /var/lib/neo4j
# Thu, 24 Aug 2023 19:40:26 GMT
VOLUME [/data /logs]
# Thu, 24 Aug 2023 19:40:26 GMT
EXPOSE 7473 7474 7687
# Thu, 24 Aug 2023 19:40:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 24 Aug 2023 19:40:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e09cb30a1ef0915a1ffb7a7e09dbfbbd6ca50b0de70ef22c1ecb37d83b229`  
		Last Modified: Wed, 16 Aug 2023 17:31:53 GMT  
		Size: 141.6 MB (141565229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac9d37a07a4e53120bd763851e062d8978d50803412dea99e178420f0b2d7c8`  
		Last Modified: Thu, 24 Aug 2023 19:41:19 GMT  
		Size: 3.9 KB (3891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c5e167f4405d40075594811b3c3e9fd7aa817f985ff364dee8d38cdb5c9696`  
		Last Modified: Thu, 24 Aug 2023 19:41:19 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d554696f9c31b37a004157ffa4d7563cc64ffffee7735420a860fa0944602280`  
		Last Modified: Thu, 24 Aug 2023 19:41:29 GMT  
		Size: 222.1 MB (222105934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:013e73d90b293a94c0c6183f3eec5647bc3108ea12fe7dd27f5b3d401806d6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2d088585c6eeccb0705f4c5ed779a893d2dd1fe0258a99ee11747f51507543bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304312416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280525afe8ac47d2d6ad3ee6f71ad4d328b463926690e5ecd1e57aa6fa67187`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:41 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:41 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:41 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce52a0e176304ac6b6d4374ad17c186f2a0b145fb1946336bdb41a2b5b9fe0a`  
		Last Modified: Thu, 17 Aug 2023 10:12:01 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e559c986adac717d7ee3ba0fca93c12dc4e44b5e6325755dfa33c33a216cedaa`  
		Last Modified: Thu, 17 Aug 2023 10:12:08 GMT  
		Size: 113.7 MB (113704390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e46a4e4523b846c406c8df4a0c5b00f46e012cf5a335a4c56b5abdee56508d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301283576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5583646a630dc67b5478bcf12d494f23d9d3111bee3beea3312d2dd5cdb25595`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:42 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:46 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:46 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3669de5dd9b71b5171db0ea80172e0434dd626fff921721810bdcd4da1abc`  
		Last Modified: Thu, 17 Aug 2023 01:28:55 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af814bcc2ddcf3c718c73ebb2ef5df96d2d0b35e9863c7dbf681ae9d5bae8a67`  
		Last Modified: Thu, 17 Aug 2023 01:29:01 GMT  
		Size: 113.7 MB (113704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:fe681efbace11755292b13da8c8e2585870451a72c81f90ea0a8d637ae2828f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d3abad92ee0cafe6a481bf9d235f12b6e8f7acaa04d7c67038fe865639e6db5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579904744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efd586979f1ebc1a35fc09d15a94f067cedd64a638eaf4bdd504d4d75c2c506`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:09:06 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:09:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:24 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:24 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:24 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fdeab8aed9835947830d9f184f6f21b4bafe21caa8bf5af67f8ae08a0d967`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e081f28f54fed3c9c3273fb8c5fbcf6769a7aa3c5d10cc28d228150a358f8`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2157a75d21111b9df98878ce2133fc98e4c4b43f0817868283a1810de8535d`  
		Last Modified: Thu, 17 Aug 2023 10:11:39 GMT  
		Size: 403.7 MB (403700128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:abcf760aa951a2d46741862c665adaf396d8bfdedfaaf53f4bfb866d744fb5a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577205982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498c6b3fff483a76f8a78e912d01038f6b06995cb1fe860c8745666a6397bb4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:56 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:26:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:25 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:25 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bdfd7bf6c0410f6c5d3d5b1c09367d8da9a6b6dbb9a8600659fa1f060803f9`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc332bdc9cb98200cd3a234f8e71d7517e5525f507efe285373f227af49de3`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5645b7152fbaf5c18bf624421781149836837a9c5d71f898c771c42234f28384`  
		Last Modified: Thu, 17 Aug 2023 01:28:33 GMT  
		Size: 403.6 MB (403591821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:fe681efbace11755292b13da8c8e2585870451a72c81f90ea0a8d637ae2828f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d3abad92ee0cafe6a481bf9d235f12b6e8f7acaa04d7c67038fe865639e6db5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579904744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efd586979f1ebc1a35fc09d15a94f067cedd64a638eaf4bdd504d4d75c2c506`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:09:06 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:09:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:24 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:24 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:24 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fdeab8aed9835947830d9f184f6f21b4bafe21caa8bf5af67f8ae08a0d967`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e081f28f54fed3c9c3273fb8c5fbcf6769a7aa3c5d10cc28d228150a358f8`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2157a75d21111b9df98878ce2133fc98e4c4b43f0817868283a1810de8535d`  
		Last Modified: Thu, 17 Aug 2023 10:11:39 GMT  
		Size: 403.7 MB (403700128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:abcf760aa951a2d46741862c665adaf396d8bfdedfaaf53f4bfb866d744fb5a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577205982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498c6b3fff483a76f8a78e912d01038f6b06995cb1fe860c8745666a6397bb4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:56 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:26:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:25 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:25 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bdfd7bf6c0410f6c5d3d5b1c09367d8da9a6b6dbb9a8600659fa1f060803f9`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc332bdc9cb98200cd3a234f8e71d7517e5525f507efe285373f227af49de3`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5645b7152fbaf5c18bf624421781149836837a9c5d71f898c771c42234f28384`  
		Last Modified: Thu, 17 Aug 2023 01:28:33 GMT  
		Size: 403.6 MB (403591821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a45c6da4805bafb237b91b9f3e0910ef6bd6bead7e364a3e8f3713e0eeac0365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7567f30078de3e7c86c9311066b035123062a003b509c002feb0711843247eed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.5 MB (590500929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dcb6ac70b668d764d3160e90cec73a0ca2a7def6e1f9dcd00979ee789b6a19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:46 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:58 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:58 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:58 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1666f6c0c2d66090ff9dd23929078230c98ab828c9448f895328db5ddd96c1`  
		Last Modified: Thu, 17 Aug 2023 10:12:33 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb83bdf34348eeaf6501c57a1057dfa5b6adfdcc38a61f03f2dbad9fb4e6b584`  
		Last Modified: Thu, 17 Aug 2023 10:12:54 GMT  
		Size: 399.9 MB (399892906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5db3cad3d34b4680e70762d88126cb5fb450465fa721b73138170f26c75d9ff5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.5 MB (587472173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673c50148db3dd955f7449f7b19d05a324dfeb168fc879f9edf8853a4b138594`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:27:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:27:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:27:01 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:27:01 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:27:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:27:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282ab0089796bc90ec405471494fce4aeb906f83c41d56f4eee5b53f7b7fe7c`  
		Last Modified: Thu, 17 Aug 2023 01:29:22 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a067445f68579ce62d30a406c181f714a8f6ef4ae77461bbcf681b9ae3709a76`  
		Last Modified: Thu, 17 Aug 2023 01:29:40 GMT  
		Size: 399.9 MB (399892982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:013e73d90b293a94c0c6183f3eec5647bc3108ea12fe7dd27f5b3d401806d6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2d088585c6eeccb0705f4c5ed779a893d2dd1fe0258a99ee11747f51507543bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304312416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280525afe8ac47d2d6ad3ee6f71ad4d328b463926690e5ecd1e57aa6fa67187`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:41 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:41 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:41 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce52a0e176304ac6b6d4374ad17c186f2a0b145fb1946336bdb41a2b5b9fe0a`  
		Last Modified: Thu, 17 Aug 2023 10:12:01 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e559c986adac717d7ee3ba0fca93c12dc4e44b5e6325755dfa33c33a216cedaa`  
		Last Modified: Thu, 17 Aug 2023 10:12:08 GMT  
		Size: 113.7 MB (113704390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e46a4e4523b846c406c8df4a0c5b00f46e012cf5a335a4c56b5abdee56508d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301283576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5583646a630dc67b5478bcf12d494f23d9d3111bee3beea3312d2dd5cdb25595`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:42 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:46 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:46 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3669de5dd9b71b5171db0ea80172e0434dd626fff921721810bdcd4da1abc`  
		Last Modified: Thu, 17 Aug 2023 01:28:55 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af814bcc2ddcf3c718c73ebb2ef5df96d2d0b35e9863c7dbf681ae9d5bae8a67`  
		Last Modified: Thu, 17 Aug 2023 01:29:01 GMT  
		Size: 113.7 MB (113704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11-bullseye`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11-community`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11-community` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11-community-bullseye`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11-community-ubi8`

```console
$ docker pull neo4j@sha256:013e73d90b293a94c0c6183f3eec5647bc3108ea12fe7dd27f5b3d401806d6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2d088585c6eeccb0705f4c5ed779a893d2dd1fe0258a99ee11747f51507543bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304312416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280525afe8ac47d2d6ad3ee6f71ad4d328b463926690e5ecd1e57aa6fa67187`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:41 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:41 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:41 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce52a0e176304ac6b6d4374ad17c186f2a0b145fb1946336bdb41a2b5b9fe0a`  
		Last Modified: Thu, 17 Aug 2023 10:12:01 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e559c986adac717d7ee3ba0fca93c12dc4e44b5e6325755dfa33c33a216cedaa`  
		Last Modified: Thu, 17 Aug 2023 10:12:08 GMT  
		Size: 113.7 MB (113704390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e46a4e4523b846c406c8df4a0c5b00f46e012cf5a335a4c56b5abdee56508d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301283576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5583646a630dc67b5478bcf12d494f23d9d3111bee3beea3312d2dd5cdb25595`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:42 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:46 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:46 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3669de5dd9b71b5171db0ea80172e0434dd626fff921721810bdcd4da1abc`  
		Last Modified: Thu, 17 Aug 2023 01:28:55 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af814bcc2ddcf3c718c73ebb2ef5df96d2d0b35e9863c7dbf681ae9d5bae8a67`  
		Last Modified: Thu, 17 Aug 2023 01:29:01 GMT  
		Size: 113.7 MB (113704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11-enterprise`

```console
$ docker pull neo4j@sha256:fe681efbace11755292b13da8c8e2585870451a72c81f90ea0a8d637ae2828f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d3abad92ee0cafe6a481bf9d235f12b6e8f7acaa04d7c67038fe865639e6db5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579904744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efd586979f1ebc1a35fc09d15a94f067cedd64a638eaf4bdd504d4d75c2c506`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:09:06 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:09:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:24 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:24 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:24 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fdeab8aed9835947830d9f184f6f21b4bafe21caa8bf5af67f8ae08a0d967`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e081f28f54fed3c9c3273fb8c5fbcf6769a7aa3c5d10cc28d228150a358f8`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2157a75d21111b9df98878ce2133fc98e4c4b43f0817868283a1810de8535d`  
		Last Modified: Thu, 17 Aug 2023 10:11:39 GMT  
		Size: 403.7 MB (403700128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:abcf760aa951a2d46741862c665adaf396d8bfdedfaaf53f4bfb866d744fb5a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577205982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498c6b3fff483a76f8a78e912d01038f6b06995cb1fe860c8745666a6397bb4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:56 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:26:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:25 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:25 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bdfd7bf6c0410f6c5d3d5b1c09367d8da9a6b6dbb9a8600659fa1f060803f9`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc332bdc9cb98200cd3a234f8e71d7517e5525f507efe285373f227af49de3`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5645b7152fbaf5c18bf624421781149836837a9c5d71f898c771c42234f28384`  
		Last Modified: Thu, 17 Aug 2023 01:28:33 GMT  
		Size: 403.6 MB (403591821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:fe681efbace11755292b13da8c8e2585870451a72c81f90ea0a8d637ae2828f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d3abad92ee0cafe6a481bf9d235f12b6e8f7acaa04d7c67038fe865639e6db5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579904744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efd586979f1ebc1a35fc09d15a94f067cedd64a638eaf4bdd504d4d75c2c506`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:09:06 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:09:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:24 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:24 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:24 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fdeab8aed9835947830d9f184f6f21b4bafe21caa8bf5af67f8ae08a0d967`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e081f28f54fed3c9c3273fb8c5fbcf6769a7aa3c5d10cc28d228150a358f8`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2157a75d21111b9df98878ce2133fc98e4c4b43f0817868283a1810de8535d`  
		Last Modified: Thu, 17 Aug 2023 10:11:39 GMT  
		Size: 403.7 MB (403700128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:abcf760aa951a2d46741862c665adaf396d8bfdedfaaf53f4bfb866d744fb5a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577205982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498c6b3fff483a76f8a78e912d01038f6b06995cb1fe860c8745666a6397bb4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:56 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:26:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:25 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:25 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bdfd7bf6c0410f6c5d3d5b1c09367d8da9a6b6dbb9a8600659fa1f060803f9`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc332bdc9cb98200cd3a234f8e71d7517e5525f507efe285373f227af49de3`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5645b7152fbaf5c18bf624421781149836837a9c5d71f898c771c42234f28384`  
		Last Modified: Thu, 17 Aug 2023 01:28:33 GMT  
		Size: 403.6 MB (403591821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a45c6da4805bafb237b91b9f3e0910ef6bd6bead7e364a3e8f3713e0eeac0365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7567f30078de3e7c86c9311066b035123062a003b509c002feb0711843247eed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.5 MB (590500929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dcb6ac70b668d764d3160e90cec73a0ca2a7def6e1f9dcd00979ee789b6a19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:46 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:58 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:58 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:58 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1666f6c0c2d66090ff9dd23929078230c98ab828c9448f895328db5ddd96c1`  
		Last Modified: Thu, 17 Aug 2023 10:12:33 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb83bdf34348eeaf6501c57a1057dfa5b6adfdcc38a61f03f2dbad9fb4e6b584`  
		Last Modified: Thu, 17 Aug 2023 10:12:54 GMT  
		Size: 399.9 MB (399892906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5db3cad3d34b4680e70762d88126cb5fb450465fa721b73138170f26c75d9ff5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.5 MB (587472173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673c50148db3dd955f7449f7b19d05a324dfeb168fc879f9edf8853a4b138594`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:27:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:27:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:27:01 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:27:01 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:27:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:27:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282ab0089796bc90ec405471494fce4aeb906f83c41d56f4eee5b53f7b7fe7c`  
		Last Modified: Thu, 17 Aug 2023 01:29:22 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a067445f68579ce62d30a406c181f714a8f6ef4ae77461bbcf681b9ae3709a76`  
		Last Modified: Thu, 17 Aug 2023 01:29:40 GMT  
		Size: 399.9 MB (399892982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11-ubi8`

```console
$ docker pull neo4j@sha256:013e73d90b293a94c0c6183f3eec5647bc3108ea12fe7dd27f5b3d401806d6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2d088585c6eeccb0705f4c5ed779a893d2dd1fe0258a99ee11747f51507543bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304312416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280525afe8ac47d2d6ad3ee6f71ad4d328b463926690e5ecd1e57aa6fa67187`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:41 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:41 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:41 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce52a0e176304ac6b6d4374ad17c186f2a0b145fb1946336bdb41a2b5b9fe0a`  
		Last Modified: Thu, 17 Aug 2023 10:12:01 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e559c986adac717d7ee3ba0fca93c12dc4e44b5e6325755dfa33c33a216cedaa`  
		Last Modified: Thu, 17 Aug 2023 10:12:08 GMT  
		Size: 113.7 MB (113704390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e46a4e4523b846c406c8df4a0c5b00f46e012cf5a335a4c56b5abdee56508d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301283576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5583646a630dc67b5478bcf12d494f23d9d3111bee3beea3312d2dd5cdb25595`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:42 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:46 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:46 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3669de5dd9b71b5171db0ea80172e0434dd626fff921721810bdcd4da1abc`  
		Last Modified: Thu, 17 Aug 2023 01:28:55 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af814bcc2ddcf3c718c73ebb2ef5df96d2d0b35e9863c7dbf681ae9d5bae8a67`  
		Last Modified: Thu, 17 Aug 2023 01:29:01 GMT  
		Size: 113.7 MB (113704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11.0`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11.0` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11.0-bullseye`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11.0-community`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11.0-community-bullseye`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11.0-community-ubi8`

```console
$ docker pull neo4j@sha256:013e73d90b293a94c0c6183f3eec5647bc3108ea12fe7dd27f5b3d401806d6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2d088585c6eeccb0705f4c5ed779a893d2dd1fe0258a99ee11747f51507543bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304312416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280525afe8ac47d2d6ad3ee6f71ad4d328b463926690e5ecd1e57aa6fa67187`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:41 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:41 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:41 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce52a0e176304ac6b6d4374ad17c186f2a0b145fb1946336bdb41a2b5b9fe0a`  
		Last Modified: Thu, 17 Aug 2023 10:12:01 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e559c986adac717d7ee3ba0fca93c12dc4e44b5e6325755dfa33c33a216cedaa`  
		Last Modified: Thu, 17 Aug 2023 10:12:08 GMT  
		Size: 113.7 MB (113704390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e46a4e4523b846c406c8df4a0c5b00f46e012cf5a335a4c56b5abdee56508d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301283576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5583646a630dc67b5478bcf12d494f23d9d3111bee3beea3312d2dd5cdb25595`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:42 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:46 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:46 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3669de5dd9b71b5171db0ea80172e0434dd626fff921721810bdcd4da1abc`  
		Last Modified: Thu, 17 Aug 2023 01:28:55 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af814bcc2ddcf3c718c73ebb2ef5df96d2d0b35e9863c7dbf681ae9d5bae8a67`  
		Last Modified: Thu, 17 Aug 2023 01:29:01 GMT  
		Size: 113.7 MB (113704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11.0-enterprise`

```console
$ docker pull neo4j@sha256:fe681efbace11755292b13da8c8e2585870451a72c81f90ea0a8d637ae2828f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d3abad92ee0cafe6a481bf9d235f12b6e8f7acaa04d7c67038fe865639e6db5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579904744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efd586979f1ebc1a35fc09d15a94f067cedd64a638eaf4bdd504d4d75c2c506`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:09:06 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:09:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:24 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:24 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:24 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fdeab8aed9835947830d9f184f6f21b4bafe21caa8bf5af67f8ae08a0d967`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e081f28f54fed3c9c3273fb8c5fbcf6769a7aa3c5d10cc28d228150a358f8`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2157a75d21111b9df98878ce2133fc98e4c4b43f0817868283a1810de8535d`  
		Last Modified: Thu, 17 Aug 2023 10:11:39 GMT  
		Size: 403.7 MB (403700128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:abcf760aa951a2d46741862c665adaf396d8bfdedfaaf53f4bfb866d744fb5a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577205982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498c6b3fff483a76f8a78e912d01038f6b06995cb1fe860c8745666a6397bb4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:56 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:26:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:25 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:25 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bdfd7bf6c0410f6c5d3d5b1c09367d8da9a6b6dbb9a8600659fa1f060803f9`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc332bdc9cb98200cd3a234f8e71d7517e5525f507efe285373f227af49de3`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5645b7152fbaf5c18bf624421781149836837a9c5d71f898c771c42234f28384`  
		Last Modified: Thu, 17 Aug 2023 01:28:33 GMT  
		Size: 403.6 MB (403591821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:fe681efbace11755292b13da8c8e2585870451a72c81f90ea0a8d637ae2828f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d3abad92ee0cafe6a481bf9d235f12b6e8f7acaa04d7c67038fe865639e6db5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579904744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efd586979f1ebc1a35fc09d15a94f067cedd64a638eaf4bdd504d4d75c2c506`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:09:06 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:09:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:24 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:24 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:24 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fdeab8aed9835947830d9f184f6f21b4bafe21caa8bf5af67f8ae08a0d967`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e081f28f54fed3c9c3273fb8c5fbcf6769a7aa3c5d10cc28d228150a358f8`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2157a75d21111b9df98878ce2133fc98e4c4b43f0817868283a1810de8535d`  
		Last Modified: Thu, 17 Aug 2023 10:11:39 GMT  
		Size: 403.7 MB (403700128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:abcf760aa951a2d46741862c665adaf396d8bfdedfaaf53f4bfb866d744fb5a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577205982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498c6b3fff483a76f8a78e912d01038f6b06995cb1fe860c8745666a6397bb4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:56 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:26:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:25 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:25 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bdfd7bf6c0410f6c5d3d5b1c09367d8da9a6b6dbb9a8600659fa1f060803f9`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc332bdc9cb98200cd3a234f8e71d7517e5525f507efe285373f227af49de3`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5645b7152fbaf5c18bf624421781149836837a9c5d71f898c771c42234f28384`  
		Last Modified: Thu, 17 Aug 2023 01:28:33 GMT  
		Size: 403.6 MB (403591821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a45c6da4805bafb237b91b9f3e0910ef6bd6bead7e364a3e8f3713e0eeac0365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7567f30078de3e7c86c9311066b035123062a003b509c002feb0711843247eed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.5 MB (590500929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dcb6ac70b668d764d3160e90cec73a0ca2a7def6e1f9dcd00979ee789b6a19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:46 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:58 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:58 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:58 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1666f6c0c2d66090ff9dd23929078230c98ab828c9448f895328db5ddd96c1`  
		Last Modified: Thu, 17 Aug 2023 10:12:33 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb83bdf34348eeaf6501c57a1057dfa5b6adfdcc38a61f03f2dbad9fb4e6b584`  
		Last Modified: Thu, 17 Aug 2023 10:12:54 GMT  
		Size: 399.9 MB (399892906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5db3cad3d34b4680e70762d88126cb5fb450465fa721b73138170f26c75d9ff5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.5 MB (587472173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673c50148db3dd955f7449f7b19d05a324dfeb168fc879f9edf8853a4b138594`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:27:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:27:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:27:01 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:27:01 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:27:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:27:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282ab0089796bc90ec405471494fce4aeb906f83c41d56f4eee5b53f7b7fe7c`  
		Last Modified: Thu, 17 Aug 2023 01:29:22 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a067445f68579ce62d30a406c181f714a8f6ef4ae77461bbcf681b9ae3709a76`  
		Last Modified: Thu, 17 Aug 2023 01:29:40 GMT  
		Size: 399.9 MB (399892982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.11.0-ubi8`

```console
$ docker pull neo4j@sha256:013e73d90b293a94c0c6183f3eec5647bc3108ea12fe7dd27f5b3d401806d6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.11.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2d088585c6eeccb0705f4c5ed779a893d2dd1fe0258a99ee11747f51507543bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304312416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280525afe8ac47d2d6ad3ee6f71ad4d328b463926690e5ecd1e57aa6fa67187`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:41 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:41 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:41 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce52a0e176304ac6b6d4374ad17c186f2a0b145fb1946336bdb41a2b5b9fe0a`  
		Last Modified: Thu, 17 Aug 2023 10:12:01 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e559c986adac717d7ee3ba0fca93c12dc4e44b5e6325755dfa33c33a216cedaa`  
		Last Modified: Thu, 17 Aug 2023 10:12:08 GMT  
		Size: 113.7 MB (113704390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.11.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e46a4e4523b846c406c8df4a0c5b00f46e012cf5a335a4c56b5abdee56508d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301283576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5583646a630dc67b5478bcf12d494f23d9d3111bee3beea3312d2dd5cdb25595`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:42 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:46 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:46 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3669de5dd9b71b5171db0ea80172e0434dd626fff921721810bdcd4da1abc`  
		Last Modified: Thu, 17 Aug 2023 01:28:55 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af814bcc2ddcf3c718c73ebb2ef5df96d2d0b35e9863c7dbf681ae9d5bae8a67`  
		Last Modified: Thu, 17 Aug 2023 01:29:01 GMT  
		Size: 113.7 MB (113704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:013e73d90b293a94c0c6183f3eec5647bc3108ea12fe7dd27f5b3d401806d6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2d088585c6eeccb0705f4c5ed779a893d2dd1fe0258a99ee11747f51507543bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304312416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280525afe8ac47d2d6ad3ee6f71ad4d328b463926690e5ecd1e57aa6fa67187`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:41 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:41 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:41 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce52a0e176304ac6b6d4374ad17c186f2a0b145fb1946336bdb41a2b5b9fe0a`  
		Last Modified: Thu, 17 Aug 2023 10:12:01 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e559c986adac717d7ee3ba0fca93c12dc4e44b5e6325755dfa33c33a216cedaa`  
		Last Modified: Thu, 17 Aug 2023 10:12:08 GMT  
		Size: 113.7 MB (113704390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e46a4e4523b846c406c8df4a0c5b00f46e012cf5a335a4c56b5abdee56508d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301283576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5583646a630dc67b5478bcf12d494f23d9d3111bee3beea3312d2dd5cdb25595`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:42 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:46 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:46 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3669de5dd9b71b5171db0ea80172e0434dd626fff921721810bdcd4da1abc`  
		Last Modified: Thu, 17 Aug 2023 01:28:55 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af814bcc2ddcf3c718c73ebb2ef5df96d2d0b35e9863c7dbf681ae9d5bae8a67`  
		Last Modified: Thu, 17 Aug 2023 01:29:01 GMT  
		Size: 113.7 MB (113704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:fe681efbace11755292b13da8c8e2585870451a72c81f90ea0a8d637ae2828f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d3abad92ee0cafe6a481bf9d235f12b6e8f7acaa04d7c67038fe865639e6db5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579904744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efd586979f1ebc1a35fc09d15a94f067cedd64a638eaf4bdd504d4d75c2c506`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:09:06 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:09:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:24 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:24 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:24 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fdeab8aed9835947830d9f184f6f21b4bafe21caa8bf5af67f8ae08a0d967`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e081f28f54fed3c9c3273fb8c5fbcf6769a7aa3c5d10cc28d228150a358f8`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2157a75d21111b9df98878ce2133fc98e4c4b43f0817868283a1810de8535d`  
		Last Modified: Thu, 17 Aug 2023 10:11:39 GMT  
		Size: 403.7 MB (403700128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:abcf760aa951a2d46741862c665adaf396d8bfdedfaaf53f4bfb866d744fb5a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577205982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498c6b3fff483a76f8a78e912d01038f6b06995cb1fe860c8745666a6397bb4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:56 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:26:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:25 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:25 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bdfd7bf6c0410f6c5d3d5b1c09367d8da9a6b6dbb9a8600659fa1f060803f9`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc332bdc9cb98200cd3a234f8e71d7517e5525f507efe285373f227af49de3`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5645b7152fbaf5c18bf624421781149836837a9c5d71f898c771c42234f28384`  
		Last Modified: Thu, 17 Aug 2023 01:28:33 GMT  
		Size: 403.6 MB (403591821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:fe681efbace11755292b13da8c8e2585870451a72c81f90ea0a8d637ae2828f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d3abad92ee0cafe6a481bf9d235f12b6e8f7acaa04d7c67038fe865639e6db5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579904744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efd586979f1ebc1a35fc09d15a94f067cedd64a638eaf4bdd504d4d75c2c506`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:09:06 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:09:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:24 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:24 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:24 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fdeab8aed9835947830d9f184f6f21b4bafe21caa8bf5af67f8ae08a0d967`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e081f28f54fed3c9c3273fb8c5fbcf6769a7aa3c5d10cc28d228150a358f8`  
		Last Modified: Thu, 17 Aug 2023 10:11:21 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2157a75d21111b9df98878ce2133fc98e4c4b43f0817868283a1810de8535d`  
		Last Modified: Thu, 17 Aug 2023 10:11:39 GMT  
		Size: 403.7 MB (403700128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:abcf760aa951a2d46741862c665adaf396d8bfdedfaaf53f4bfb866d744fb5a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577205982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498c6b3fff483a76f8a78e912d01038f6b06995cb1fe860c8745666a6397bb4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:56 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:26:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:25 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:25 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bdfd7bf6c0410f6c5d3d5b1c09367d8da9a6b6dbb9a8600659fa1f060803f9`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc332bdc9cb98200cd3a234f8e71d7517e5525f507efe285373f227af49de3`  
		Last Modified: Thu, 17 Aug 2023 01:28:16 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5645b7152fbaf5c18bf624421781149836837a9c5d71f898c771c42234f28384`  
		Last Modified: Thu, 17 Aug 2023 01:28:33 GMT  
		Size: 403.6 MB (403591821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a45c6da4805bafb237b91b9f3e0910ef6bd6bead7e364a3e8f3713e0eeac0365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7567f30078de3e7c86c9311066b035123062a003b509c002feb0711843247eed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.5 MB (590500929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dcb6ac70b668d764d3160e90cec73a0ca2a7def6e1f9dcd00979ee789b6a19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:46 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:58 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:58 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:58 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1666f6c0c2d66090ff9dd23929078230c98ab828c9448f895328db5ddd96c1`  
		Last Modified: Thu, 17 Aug 2023 10:12:33 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb83bdf34348eeaf6501c57a1057dfa5b6adfdcc38a61f03f2dbad9fb4e6b584`  
		Last Modified: Thu, 17 Aug 2023 10:12:54 GMT  
		Size: 399.9 MB (399892906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5db3cad3d34b4680e70762d88126cb5fb450465fa721b73138170f26c75d9ff5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.5 MB (587472173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673c50148db3dd955f7449f7b19d05a324dfeb168fc879f9edf8853a4b138594`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0de7579b9b307dbd24793368415ccac799911705ede4a8f70275e4b4eb94c05c NEO4J_TARBALL=neo4j-enterprise-5.11.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:27:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:27:01 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:27:01 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:27:01 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:27:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:27:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282ab0089796bc90ec405471494fce4aeb906f83c41d56f4eee5b53f7b7fe7c`  
		Last Modified: Thu, 17 Aug 2023 01:29:22 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a067445f68579ce62d30a406c181f714a8f6ef4ae77461bbcf681b9ae3709a76`  
		Last Modified: Thu, 17 Aug 2023 01:29:40 GMT  
		Size: 399.9 MB (399892982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:b56fd7c0da7d717dd4b8668f0deb9a2e6369c48b05caab75f4bb8e8e3afc5c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:acad44c4c0ce675745008de8cc5b83ecbe88545d3298bfaac0bfe6504ee16381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293720172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5b693a4dbaf98473e9d295f2f8696286a1fe8c7d722a0d680439b8be1c19f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:12 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:08:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:08:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 10:08:45 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:08:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 10:08:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:08:59 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:08:59 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:00 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f19d3c0c76607d38f469ea69cdeea9a0f589af42c6145f4530a3ae325eaef2`  
		Last Modified: Wed, 16 Aug 2023 17:03:52 GMT  
		Size: 144.8 MB (144773731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45bf0a420b65db47d2998894a55e2adcaf6681afb0d2647eddc955ebc950b8`  
		Last Modified: Thu, 17 Aug 2023 10:10:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f163608e839f1622c2ee393975b5de2f94e77e557fd87b141126922e3ed9f17e`  
		Last Modified: Thu, 17 Aug 2023 10:10:39 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7016299ad80373dfbf5b3aba89577d434fb3107abdc73a028fe71b436e3d86f`  
		Last Modified: Thu, 17 Aug 2023 10:10:45 GMT  
		Size: 117.5 MB (117515558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74f04472ca76e214b38413f9279ab38e560f06ef423605e7591494f939f26b22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291022736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7035a56efda51b7c25845c37e854a1725379b06089d1dccd720a3ef570e8f6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:25:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:25:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 17 Aug 2023 01:25:40 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 01:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:25:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:25:52 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:25:52 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3c45056d1f2d245cc4191f75a1c781742c9ef7c945ce0eb49741ff03afd7d5`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd67db71629e8e1e567670cc55d5b342eb40c6ae2dabe9876ad7ec90888abb6`  
		Last Modified: Thu, 17 Aug 2023 01:27:35 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea8fc6630778fadae75a2193c0fab3b707927f5b9701ba797b5bfd5b627c3d6`  
		Last Modified: Thu, 17 Aug 2023 01:27:42 GMT  
		Size: 117.4 MB (117408576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:013e73d90b293a94c0c6183f3eec5647bc3108ea12fe7dd27f5b3d401806d6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2d088585c6eeccb0705f4c5ed779a893d2dd1fe0258a99ee11747f51507543bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304312416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280525afe8ac47d2d6ad3ee6f71ad4d328b463926690e5ecd1e57aa6fa67187`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:34 GMT
ADD file:84dff5b0f84a1086a0a07b28849d08a18f2d658869173d376845a20a2cb34541 in / 
# Wed, 03 May 2023 15:11:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:36 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:36 GMT
ENV container oci
# Wed, 03 May 2023 15:11:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:36 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:36 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:36 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:37 GMT
ADD file:13e13737bf27853f3a47e1f55b843236868d5521b05c5fed54688856d11bd33f in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:37 GMT
ADD file:fcaeea1e052139bcd93a719356f6d30b0bd66243e25ccb0a8ed0e3b2013b5804 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:37 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:38 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:39 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 22:58:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:01:59 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Thu, 17 Aug 2023 10:09:37 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 10:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 10:09:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 10:09:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 10:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 10:09:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 10:09:41 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 10:09:41 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 10:09:41 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 10:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 10:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd9537bc52f60ded583bf06bc3a05063d4e52cbcd3d48df8c2748d454856e0`  
		Last Modified: Wed, 16 Aug 2023 17:05:18 GMT  
		Size: 144.8 MB (144773734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e5c2f204d9998525aa640a72e775a235c149aa41609053fe83c6be30bdc50`  
		Last Modified: Thu, 17 Aug 2023 10:12:02 GMT  
		Size: 6.5 MB (6535899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce52a0e176304ac6b6d4374ad17c186f2a0b145fb1946336bdb41a2b5b9fe0a`  
		Last Modified: Thu, 17 Aug 2023 10:12:01 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e559c986adac717d7ee3ba0fca93c12dc4e44b5e6325755dfa33c33a216cedaa`  
		Last Modified: Thu, 17 Aug 2023 10:12:08 GMT  
		Size: 113.7 MB (113704390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e46a4e4523b846c406c8df4a0c5b00f46e012cf5a335a4c56b5abdee56508d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301283576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5583646a630dc67b5478bcf12d494f23d9d3111bee3beea3312d2dd5cdb25595`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 15:11:05 GMT
ADD file:c1449fa3fa5e28681c0d29ba138d06c93ca3be96e038d945ac7d474f9693e797 in / 
# Wed, 03 May 2023 15:11:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 15:11:07 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 15:11:07 GMT
ADD multi:62a5ed918ba581cb28e63a96c95a2291910a696c57ec0a22b415b43695503828 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 15:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 03 May 2023 15:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 15:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 May 2023 15:11:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 15:11:07 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 May 2023 15:11:07 GMT
ENV container oci
# Wed, 03 May 2023 15:11:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:11:07 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 15:11:08 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 15:11:08 GMT
LABEL release=860
# Wed, 03 May 2023 15:11:08 GMT
ADD file:a071058fca5391f210272bff5a389267bf1c9383b47b5473dff87949a9ea8630 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-860.json 
# Wed, 03 May 2023 15:11:08 GMT
ADD file:777f5b26862de30ef41c6c5468c53fe0c949b0ac6f03cb717986596bd3afd6d3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-860 
# Wed, 03 May 2023 15:11:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T15:02:09" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-860"
# Wed, 03 May 2023 15:11:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-700b5.repo' '/etc/yum.repos.d/repo-cb269.repo'
# Wed, 03 May 2023 15:11:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 15:11:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 24 Jul 2023 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:03:36 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Thu, 17 Aug 2023 01:26:42 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Thu, 17 Aug 2023 01:26:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a206271d01ff337ab64e99a9ea90b17733416ec17c093b5be7bfb9342b0dacd NEO4J_TARBALL=neo4j-community-5.11.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 17 Aug 2023 01:26:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
# Thu, 17 Aug 2023 01:26:42 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Thu, 17 Aug 2023 01:26:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.11.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Thu, 17 Aug 2023 01:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 01:26:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 17 Aug 2023 01:26:46 GMT
VOLUME [/data /logs]
# Thu, 17 Aug 2023 01:26:46 GMT
EXPOSE 7473 7474 7687
# Thu, 17 Aug 2023 01:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 17 Aug 2023 01:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08f6a51aabcd289de7b8d70c5289e580719ee3b7d01c0c3df1914d03fd3ebde`  
		Last Modified: Wed, 16 Aug 2023 18:06:42 GMT  
		Size: 143.5 MB (143538102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bf1ec03e85f26ceccbf378dfd7452dcd10cb58982b6090f807edaf5c291eb`  
		Last Modified: Thu, 17 Aug 2023 01:28:56 GMT  
		Size: 6.5 MB (6500304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde3669de5dd9b71b5171db0ea80172e0434dd626fff921721810bdcd4da1abc`  
		Last Modified: Thu, 17 Aug 2023 01:28:55 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af814bcc2ddcf3c718c73ebb2ef5df96d2d0b35e9863c7dbf681ae9d5bae8a67`  
		Last Modified: Thu, 17 Aug 2023 01:29:01 GMT  
		Size: 113.7 MB (113704380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
