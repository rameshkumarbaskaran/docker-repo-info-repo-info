<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.3`](#neo4j43)
-	[`neo4j:4.3-community`](#neo4j43-community)
-	[`neo4j:4.3-enterprise`](#neo4j43-enterprise)
-	[`neo4j:4.3.15`](#neo4j4315)
-	[`neo4j:4.3.15-community`](#neo4j4315-community)
-	[`neo4j:4.3.15-enterprise`](#neo4j4315-enterprise)
-	[`neo4j:4.3.16`](#neo4j4316)
-	[`neo4j:4.3.16-community`](#neo4j4316-community)
-	[`neo4j:4.3.16-enterprise`](#neo4j4316-enterprise)
-	[`neo4j:4.3.17`](#neo4j4317)
-	[`neo4j:4.3.17-community`](#neo4j4317-community)
-	[`neo4j:4.3.17-enterprise`](#neo4j4317-enterprise)
-	[`neo4j:4.3.18`](#neo4j4318)
-	[`neo4j:4.3.18-community`](#neo4j4318-community)
-	[`neo4j:4.3.18-enterprise`](#neo4j4318-enterprise)
-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.10`](#neo4j4410)
-	[`neo4j:4.4.10-community`](#neo4j4410-community)
-	[`neo4j:4.4.10-enterprise`](#neo4j4410-enterprise)
-	[`neo4j:4.4.11`](#neo4j4411)
-	[`neo4j:4.4.11-community`](#neo4j4411-community)
-	[`neo4j:4.4.11-enterprise`](#neo4j4411-enterprise)
-	[`neo4j:4.4.9`](#neo4j449)
-	[`neo4j:4.4.9-community`](#neo4j449-community)
-	[`neo4j:4.4.9-enterprise`](#neo4j449-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.3`

```console
$ docker pull neo4j@sha256:6fe306b6600cc7303f212bb2e9b06c82e8a8f12346c4870cf7d02c93a3785621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3` - linux; amd64

```console
$ docker pull neo4j@sha256:50296868c3903216fd398da1af6797da6c27d89555f19c82d53e501756e928b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359803572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db397f9ed9b7948386f8fc7b7db735cbdf59f5261ee93647b24ea3ac19886684`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:21:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4d96649dabfaecb9bb05ef3e511c1ac39c4795621ad4bd2a7aadebf63892e39f NEO4J_TARBALL=neo4j-community-4.3.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:21:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
# Tue, 13 Sep 2022 06:21:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:21:09 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Tue, 13 Sep 2022 06:21:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:21:25 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:21:25 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:21:25 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:21:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:21:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9064153c1d0dadfbbd043c63d8937eaf3915a306ea65c8702268ca2edadb0`  
		Last Modified: Tue, 13 Sep 2022 06:26:43 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4558dfa0f17709499a6b24c8c2c06c4b3b218525307763bf73262b18ed0d6bd3`  
		Last Modified: Tue, 13 Sep 2022 06:26:43 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc3a7c4d479d5d4d7317944aa9311d3d2558b28ae92dbce2ffad065b50aa1a`  
		Last Modified: Tue, 13 Sep 2022 06:26:50 GMT  
		Size: 130.3 MB (130263083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-community`

```console
$ docker pull neo4j@sha256:6fe306b6600cc7303f212bb2e9b06c82e8a8f12346c4870cf7d02c93a3785621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-community` - linux; amd64

```console
$ docker pull neo4j@sha256:50296868c3903216fd398da1af6797da6c27d89555f19c82d53e501756e928b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359803572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db397f9ed9b7948386f8fc7b7db735cbdf59f5261ee93647b24ea3ac19886684`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:21:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4d96649dabfaecb9bb05ef3e511c1ac39c4795621ad4bd2a7aadebf63892e39f NEO4J_TARBALL=neo4j-community-4.3.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:21:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
# Tue, 13 Sep 2022 06:21:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:21:09 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Tue, 13 Sep 2022 06:21:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:21:25 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:21:25 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:21:25 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:21:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:21:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9064153c1d0dadfbbd043c63d8937eaf3915a306ea65c8702268ca2edadb0`  
		Last Modified: Tue, 13 Sep 2022 06:26:43 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4558dfa0f17709499a6b24c8c2c06c4b3b218525307763bf73262b18ed0d6bd3`  
		Last Modified: Tue, 13 Sep 2022 06:26:43 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc3a7c4d479d5d4d7317944aa9311d3d2558b28ae92dbce2ffad065b50aa1a`  
		Last Modified: Tue, 13 Sep 2022 06:26:50 GMT  
		Size: 130.3 MB (130263083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-enterprise`

```console
$ docker pull neo4j@sha256:d45ac0ea6cedb631c38cba0abd99ad5e2bfb5a9daa356b731831ed641027e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:01ea282edbe8d05d09b1320e9476729b9fc63370739172fa0adf2dc225a80b7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390282294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffece00dc35c0d9dd8065aec18ac9410496436aaebc2eec40ad1e0a0ec5046ae`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:21:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=01269489006212bd8225eb8e9c0c26e2af1ba350d8e07372409cc4c2c0aa8d76 NEO4J_TARBALL=neo4j-enterprise-4.3.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:21:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.18-unix.tar.gz
# Tue, 13 Sep 2022 06:21:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:21:30 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Tue, 13 Sep 2022 06:21:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:21:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:21:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:21:48 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:21:48 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:21:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:21:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eabb66f7f190ffbf5da75ed1a0756bb48400410f567baa4c06c1018aa6ba3d`  
		Last Modified: Tue, 13 Sep 2022 06:27:06 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de845723850b43e8e528c0af092b9cce14cb9add46dbeaaac3e0c3b3dc11dc95`  
		Last Modified: Tue, 13 Sep 2022 06:27:06 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ef4442086c718ba9be8e80ffd2a4df666038a330f496327b149f0b006525bd`  
		Last Modified: Tue, 13 Sep 2022 06:27:14 GMT  
		Size: 160.7 MB (160741805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.15`

```console
$ docker pull neo4j@sha256:ddd3a00f634a8ff4995c925ae48d5322f7288eba35ea68f229957be030a203cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.15` - linux; amd64

```console
$ docker pull neo4j@sha256:2b30e1018e665efc5bfc8b12db57be7f38174eb9288c5393ff9ce48542d43ef3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357906171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd076d183e01712f035fb536cb84126bbf8c2b1da902be49a2a0fd8a50ddc81`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=09bfaf1b60bc3498133ef10a7322c5edd66077e7dae0234415ef1d41c4315f36 NEO4J_TARBALL=neo4j-community-4.3.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:23:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.15-unix.tar.gz
# Tue, 13 Sep 2022 06:23:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:23:18 GMT
COPY multi:7f654dae9c34c4836d2dba726eda4454b4ec5547ee00cb65a6d0f4e9a5ba930b in /startup/ 
# Tue, 13 Sep 2022 06:23:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:23:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:23:31 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:23:32 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:23:32 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:23:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:23:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d18650278313a2fd8414dbcf01f77cc3bd1a3d23c4db09679715f0ad49b52`  
		Last Modified: Tue, 13 Sep 2022 06:28:30 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc9568550728339aa793caba2d7e2093e73ee94c009ba63f91adda1fbc144ee`  
		Last Modified: Tue, 13 Sep 2022 06:28:30 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5dfd021450b442c308469f2a0fd5917bb6f80446522be11e02c9a74a335e97`  
		Last Modified: Tue, 13 Sep 2022 06:28:37 GMT  
		Size: 128.4 MB (128365683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.15-community`

```console
$ docker pull neo4j@sha256:ddd3a00f634a8ff4995c925ae48d5322f7288eba35ea68f229957be030a203cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.15-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2b30e1018e665efc5bfc8b12db57be7f38174eb9288c5393ff9ce48542d43ef3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357906171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd076d183e01712f035fb536cb84126bbf8c2b1da902be49a2a0fd8a50ddc81`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=09bfaf1b60bc3498133ef10a7322c5edd66077e7dae0234415ef1d41c4315f36 NEO4J_TARBALL=neo4j-community-4.3.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:23:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.15-unix.tar.gz
# Tue, 13 Sep 2022 06:23:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:23:18 GMT
COPY multi:7f654dae9c34c4836d2dba726eda4454b4ec5547ee00cb65a6d0f4e9a5ba930b in /startup/ 
# Tue, 13 Sep 2022 06:23:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:23:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:23:31 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:23:32 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:23:32 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:23:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:23:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d18650278313a2fd8414dbcf01f77cc3bd1a3d23c4db09679715f0ad49b52`  
		Last Modified: Tue, 13 Sep 2022 06:28:30 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc9568550728339aa793caba2d7e2093e73ee94c009ba63f91adda1fbc144ee`  
		Last Modified: Tue, 13 Sep 2022 06:28:30 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5dfd021450b442c308469f2a0fd5917bb6f80446522be11e02c9a74a335e97`  
		Last Modified: Tue, 13 Sep 2022 06:28:37 GMT  
		Size: 128.4 MB (128365683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.15-enterprise`

```console
$ docker pull neo4j@sha256:c50ca482f2a7e4a8df43015f51fdae4d9c8ff91d9530c6d3570abb4f4e40aa9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.15-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:38902c042e5388cd75b94431e751797c1fb40cc42d1c8201a5ae31c7706935ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 MB (388387483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80bc806b5273dd49dd99106821253cab099a308758ff57fb71ed74e8d4c9f27`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:23:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=baba74056f917273932675a4a797ef5f926c433c08b230224b2d9985ae41424f NEO4J_TARBALL=neo4j-enterprise-4.3.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:23:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.15-unix.tar.gz
# Tue, 13 Sep 2022 06:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:23:38 GMT
COPY multi:7f654dae9c34c4836d2dba726eda4454b4ec5547ee00cb65a6d0f4e9a5ba930b in /startup/ 
# Tue, 13 Sep 2022 06:23:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:23:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:23:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:23:52 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:23:52 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:23:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:23:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff69d5527894762ab66a15657d1e20a64d3452ca32750c8f9d73b16d71f85a2`  
		Last Modified: Tue, 13 Sep 2022 06:28:47 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d7f9b22e460440a82460cf9b1081692f4ce2827bbddc3e1633814465e41567`  
		Last Modified: Tue, 13 Sep 2022 06:28:47 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6d58eb226d19c968cc35448e68b94825d8ba887c4d03c9da2dd6c699e2981e`  
		Last Modified: Tue, 13 Sep 2022 06:28:54 GMT  
		Size: 158.8 MB (158846994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.16`

```console
$ docker pull neo4j@sha256:94d6dc154a584115b9172b136d206baf3023c3748627bbf48cdbafebf52ca65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.16` - linux; amd64

```console
$ docker pull neo4j@sha256:9418bfa8b23c9f04c7443013fa838153f48e818753e30fc0b64c36a1a07b5632
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357917542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0054305d09d1031674a1044dafda06701dec50aa1bbd49bf7844551a532776`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:22:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a51652705e4f2c443a30883a9ba25f4929b89c891c265ab26a354ee75d97c5c6 NEO4J_TARBALL=neo4j-community-4.3.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:22:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.16-unix.tar.gz
# Tue, 13 Sep 2022 06:22:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:22:34 GMT
COPY multi:7f654dae9c34c4836d2dba726eda4454b4ec5547ee00cb65a6d0f4e9a5ba930b in /startup/ 
# Tue, 13 Sep 2022 06:22:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:22:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:22:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:22:48 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:22:48 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:22:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:22:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415e1da511f3bfb7faa721b7f25bf248d78f8c0dedd3f23f50cd5d013a0fc1cd`  
		Last Modified: Tue, 13 Sep 2022 06:27:58 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2613b57b376fe41ee06b93382a941e370c53b2e9c46e747241649f7cd895d0`  
		Last Modified: Tue, 13 Sep 2022 06:27:58 GMT  
		Size: 7.6 KB (7624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d07c07b6f1375eef10f44e1c782104f7db8c28bca2650fe29b9bcb0097982a`  
		Last Modified: Tue, 13 Sep 2022 06:28:04 GMT  
		Size: 128.4 MB (128377053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.16-community`

```console
$ docker pull neo4j@sha256:94d6dc154a584115b9172b136d206baf3023c3748627bbf48cdbafebf52ca65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.16-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9418bfa8b23c9f04c7443013fa838153f48e818753e30fc0b64c36a1a07b5632
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357917542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0054305d09d1031674a1044dafda06701dec50aa1bbd49bf7844551a532776`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:22:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a51652705e4f2c443a30883a9ba25f4929b89c891c265ab26a354ee75d97c5c6 NEO4J_TARBALL=neo4j-community-4.3.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:22:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.16-unix.tar.gz
# Tue, 13 Sep 2022 06:22:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:22:34 GMT
COPY multi:7f654dae9c34c4836d2dba726eda4454b4ec5547ee00cb65a6d0f4e9a5ba930b in /startup/ 
# Tue, 13 Sep 2022 06:22:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:22:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:22:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:22:48 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:22:48 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:22:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:22:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415e1da511f3bfb7faa721b7f25bf248d78f8c0dedd3f23f50cd5d013a0fc1cd`  
		Last Modified: Tue, 13 Sep 2022 06:27:58 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2613b57b376fe41ee06b93382a941e370c53b2e9c46e747241649f7cd895d0`  
		Last Modified: Tue, 13 Sep 2022 06:27:58 GMT  
		Size: 7.6 KB (7624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d07c07b6f1375eef10f44e1c782104f7db8c28bca2650fe29b9bcb0097982a`  
		Last Modified: Tue, 13 Sep 2022 06:28:04 GMT  
		Size: 128.4 MB (128377053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.16-enterprise`

```console
$ docker pull neo4j@sha256:c63fa0b110353fa23382f2a8cec4e56335eecbdc470e5676d046cb7efe83e6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ce2c886f2e471674efb0f330696102a62822998b6338e4c385e75976a575b531
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 MB (388405267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d099eb297b1d1bc3f497bf567da2deb6275bec5ad2dd92bf2fd6bd6653d5a2be`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:22:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9b5335af913c464d0b9cb0692b496cbb2682de99b556a5d7342054824e85debe NEO4J_TARBALL=neo4j-enterprise-4.3.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:22:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.16-unix.tar.gz
# Tue, 13 Sep 2022 06:22:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:22:54 GMT
COPY multi:7f654dae9c34c4836d2dba726eda4454b4ec5547ee00cb65a6d0f4e9a5ba930b in /startup/ 
# Tue, 13 Sep 2022 06:23:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:23:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:23:12 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:23:12 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:23:12 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:23:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:23:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332b7fe369535ae2a56a54e3e8cc668d8f446ed91ec7491814d6544826197138`  
		Last Modified: Tue, 13 Sep 2022 06:28:14 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7c5dc6edd3e956ccfda7cdcc01901e7b60ed85ecf7049e2cabf2c1d4e51c9d`  
		Last Modified: Tue, 13 Sep 2022 06:28:14 GMT  
		Size: 7.6 KB (7622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3c29ff2f923a4063b4358a178802feb5898cfb7bafe45f5b0470982d6964b9`  
		Last Modified: Tue, 13 Sep 2022 06:28:22 GMT  
		Size: 158.9 MB (158864782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.17`

```console
$ docker pull neo4j@sha256:b85d89f3695f820a0542f63cb8774140e984d2b8ea87f38460f52cf56a802abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.17` - linux; amd64

```console
$ docker pull neo4j@sha256:3b8f4a3e6d77b45451180ef45cc435d39012f105f4c7ee6dc37586130de80d52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359770865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413765db58d38fcb19966f1aa3852c3785a95171f5deba577f3e11963e6969d4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:21:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9148d4cb479de4a48e1dd9acdb835f4d5074d4da2dd261fb4ec8f158782d08 NEO4J_TARBALL=neo4j-community-4.3.17-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:21:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.17-unix.tar.gz
# Tue, 13 Sep 2022 06:21:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.17-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:21:54 GMT
COPY multi:7f654dae9c34c4836d2dba726eda4454b4ec5547ee00cb65a6d0f4e9a5ba930b in /startup/ 
# Tue, 13 Sep 2022 06:22:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.17-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:22:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:22:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:22:10 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:22:10 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:22:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:22:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a9cacccaccec6cceadb496ef24dd078009b603a74731b3b992bbc8289860c1`  
		Last Modified: Tue, 13 Sep 2022 06:27:25 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c2eea2f542ac7f880f2254e6003c7283c97c26b5b227a03a9f08db92afb089`  
		Last Modified: Tue, 13 Sep 2022 06:27:25 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8007c76e8863e5ff32b2688e8af611174fa618b144b5d88a9889ac908595b26f`  
		Last Modified: Tue, 13 Sep 2022 06:27:32 GMT  
		Size: 130.2 MB (130230376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.17-community`

```console
$ docker pull neo4j@sha256:b85d89f3695f820a0542f63cb8774140e984d2b8ea87f38460f52cf56a802abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.17-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3b8f4a3e6d77b45451180ef45cc435d39012f105f4c7ee6dc37586130de80d52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359770865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413765db58d38fcb19966f1aa3852c3785a95171f5deba577f3e11963e6969d4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:21:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9148d4cb479de4a48e1dd9acdb835f4d5074d4da2dd261fb4ec8f158782d08 NEO4J_TARBALL=neo4j-community-4.3.17-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:21:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.17-unix.tar.gz
# Tue, 13 Sep 2022 06:21:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.17-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:21:54 GMT
COPY multi:7f654dae9c34c4836d2dba726eda4454b4ec5547ee00cb65a6d0f4e9a5ba930b in /startup/ 
# Tue, 13 Sep 2022 06:22:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.17-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:22:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:22:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:22:10 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:22:10 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:22:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:22:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a9cacccaccec6cceadb496ef24dd078009b603a74731b3b992bbc8289860c1`  
		Last Modified: Tue, 13 Sep 2022 06:27:25 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c2eea2f542ac7f880f2254e6003c7283c97c26b5b227a03a9f08db92afb089`  
		Last Modified: Tue, 13 Sep 2022 06:27:25 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8007c76e8863e5ff32b2688e8af611174fa618b144b5d88a9889ac908595b26f`  
		Last Modified: Tue, 13 Sep 2022 06:27:32 GMT  
		Size: 130.2 MB (130230376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.17-enterprise`

```console
$ docker pull neo4j@sha256:6e43a930426d729bf0f678581540598317c818c74d52a56f3a089847b931ccbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.17-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2f2803a194ef5d55801397b7e376fd87c9a960817e7b8ecef703c209d09f1206
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e75e69f6b51c6b4114895ead3b605e7bc7b5e83ec75b62154bc6ce9c68b1cb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:22:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=061cf9efbdeb1af81a31a419d75afd9c9c922db53a54ab2d2d6cc1f1641c3081 NEO4J_TARBALL=neo4j-enterprise-4.3.17-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:22:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.17-unix.tar.gz
# Tue, 13 Sep 2022 06:22:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.17-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:22:14 GMT
COPY multi:7f654dae9c34c4836d2dba726eda4454b4ec5547ee00cb65a6d0f4e9a5ba930b in /startup/ 
# Tue, 13 Sep 2022 06:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.17-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:22:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:22:28 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:22:28 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:22:28 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:22:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:22:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085f1798cdf6973a6d472248fbea411485143d7571d285eb1f33fb83cb3d6e02`  
		Last Modified: Tue, 13 Sep 2022 06:27:41 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c9ec3ec6402a74559a76a80fb1ad079cd5683f7a87fec53343e6f573dab2a0`  
		Last Modified: Tue, 13 Sep 2022 06:27:41 GMT  
		Size: 7.6 KB (7622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9f1038d5ea1b27161e871139c66551ca2b51bd831c88144111f77ad68b5626`  
		Last Modified: Tue, 13 Sep 2022 06:27:49 GMT  
		Size: 160.7 MB (160719329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.18`

```console
$ docker pull neo4j@sha256:6fe306b6600cc7303f212bb2e9b06c82e8a8f12346c4870cf7d02c93a3785621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.18` - linux; amd64

```console
$ docker pull neo4j@sha256:50296868c3903216fd398da1af6797da6c27d89555f19c82d53e501756e928b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359803572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db397f9ed9b7948386f8fc7b7db735cbdf59f5261ee93647b24ea3ac19886684`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:21:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4d96649dabfaecb9bb05ef3e511c1ac39c4795621ad4bd2a7aadebf63892e39f NEO4J_TARBALL=neo4j-community-4.3.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:21:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
# Tue, 13 Sep 2022 06:21:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:21:09 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Tue, 13 Sep 2022 06:21:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:21:25 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:21:25 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:21:25 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:21:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:21:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9064153c1d0dadfbbd043c63d8937eaf3915a306ea65c8702268ca2edadb0`  
		Last Modified: Tue, 13 Sep 2022 06:26:43 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4558dfa0f17709499a6b24c8c2c06c4b3b218525307763bf73262b18ed0d6bd3`  
		Last Modified: Tue, 13 Sep 2022 06:26:43 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc3a7c4d479d5d4d7317944aa9311d3d2558b28ae92dbce2ffad065b50aa1a`  
		Last Modified: Tue, 13 Sep 2022 06:26:50 GMT  
		Size: 130.3 MB (130263083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.18-community`

```console
$ docker pull neo4j@sha256:6fe306b6600cc7303f212bb2e9b06c82e8a8f12346c4870cf7d02c93a3785621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.18-community` - linux; amd64

```console
$ docker pull neo4j@sha256:50296868c3903216fd398da1af6797da6c27d89555f19c82d53e501756e928b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359803572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db397f9ed9b7948386f8fc7b7db735cbdf59f5261ee93647b24ea3ac19886684`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:21:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4d96649dabfaecb9bb05ef3e511c1ac39c4795621ad4bd2a7aadebf63892e39f NEO4J_TARBALL=neo4j-community-4.3.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:21:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
# Tue, 13 Sep 2022 06:21:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:21:09 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Tue, 13 Sep 2022 06:21:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:21:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:21:25 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:21:25 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:21:25 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:21:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:21:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9064153c1d0dadfbbd043c63d8937eaf3915a306ea65c8702268ca2edadb0`  
		Last Modified: Tue, 13 Sep 2022 06:26:43 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4558dfa0f17709499a6b24c8c2c06c4b3b218525307763bf73262b18ed0d6bd3`  
		Last Modified: Tue, 13 Sep 2022 06:26:43 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc3a7c4d479d5d4d7317944aa9311d3d2558b28ae92dbce2ffad065b50aa1a`  
		Last Modified: Tue, 13 Sep 2022 06:26:50 GMT  
		Size: 130.3 MB (130263083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.18-enterprise`

```console
$ docker pull neo4j@sha256:d45ac0ea6cedb631c38cba0abd99ad5e2bfb5a9daa356b731831ed641027e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.18-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:01ea282edbe8d05d09b1320e9476729b9fc63370739172fa0adf2dc225a80b7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390282294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffece00dc35c0d9dd8065aec18ac9410496436aaebc2eec40ad1e0a0ec5046ae`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:21:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=01269489006212bd8225eb8e9c0c26e2af1ba350d8e07372409cc4c2c0aa8d76 NEO4J_TARBALL=neo4j-enterprise-4.3.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:21:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.18-unix.tar.gz
# Tue, 13 Sep 2022 06:21:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:21:30 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Tue, 13 Sep 2022 06:21:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:21:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:21:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:21:48 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:21:48 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:21:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:21:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eabb66f7f190ffbf5da75ed1a0756bb48400410f567baa4c06c1018aa6ba3d`  
		Last Modified: Tue, 13 Sep 2022 06:27:06 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de845723850b43e8e528c0af092b9cce14cb9add46dbeaaac3e0c3b3dc11dc95`  
		Last Modified: Tue, 13 Sep 2022 06:27:06 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ef4442086c718ba9be8e80ffd2a4df666038a330f496327b149f0b006525bd`  
		Last Modified: Tue, 13 Sep 2022 06:27:14 GMT  
		Size: 160.7 MB (160741805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:87458fcd5f78d9f4865a0fe26105f5051c0c80474ba99f24526e9f3544bdf31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:661f579479c8b797d0003834e79ddbfb5b9c2c3dd8217de40d9bbc93db383905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364637415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a1d9a0810a72a006a8f822ca506bca8f876fb2b88d5a34b57119d809081859`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:18:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:18:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:02 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:02 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb31dddfa2d13c70f5477d897bfef642b8bfe97f7bd883dd3f0ca3dfcb32ca0`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dc7ddb0ef7a87943a0d3ba94880718df14f33dc6634a375c688c3373c9c464`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0773aaa17b6e48fd53393008086592cc7fb670f9152f9e32b22701db3e394d50`  
		Last Modified: Tue, 13 Sep 2022 06:24:36 GMT  
		Size: 135.1 MB (135096937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9bd45fe9178fa779fcb7bc8a43b7edfd3ae1136101fefd5fe4ab45cf35445c2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359887098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f061d4eb9dbe64f565897a40424136c50b92447196498d55748f2b42005070`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:20 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:58:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:58:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:58:32 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:58:33 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:58:34 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:58:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:58:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d71b0911348d8551faffe5939c179fba47eaed5b7c8299116de7d4952697af`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80efd2fafdcbc3ae1aa49b59f7f45ab8b177bcf37d665cad020526a19449b776`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff356c782970ba7facd49528d850c914822c707df9d7146db5b63815789c9a24`  
		Last Modified: Tue, 13 Sep 2022 07:01:49 GMT  
		Size: 135.0 MB (134953583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:87458fcd5f78d9f4865a0fe26105f5051c0c80474ba99f24526e9f3544bdf31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:661f579479c8b797d0003834e79ddbfb5b9c2c3dd8217de40d9bbc93db383905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364637415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a1d9a0810a72a006a8f822ca506bca8f876fb2b88d5a34b57119d809081859`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:18:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:18:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:02 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:02 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb31dddfa2d13c70f5477d897bfef642b8bfe97f7bd883dd3f0ca3dfcb32ca0`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dc7ddb0ef7a87943a0d3ba94880718df14f33dc6634a375c688c3373c9c464`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0773aaa17b6e48fd53393008086592cc7fb670f9152f9e32b22701db3e394d50`  
		Last Modified: Tue, 13 Sep 2022 06:24:36 GMT  
		Size: 135.1 MB (135096937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9bd45fe9178fa779fcb7bc8a43b7edfd3ae1136101fefd5fe4ab45cf35445c2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359887098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f061d4eb9dbe64f565897a40424136c50b92447196498d55748f2b42005070`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:20 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:58:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:58:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:58:32 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:58:33 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:58:34 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:58:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:58:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d71b0911348d8551faffe5939c179fba47eaed5b7c8299116de7d4952697af`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80efd2fafdcbc3ae1aa49b59f7f45ab8b177bcf37d665cad020526a19449b776`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff356c782970ba7facd49528d850c914822c707df9d7146db5b63815789c9a24`  
		Last Modified: Tue, 13 Sep 2022 07:01:49 GMT  
		Size: 135.0 MB (134953583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:53544639ee1fa746724b266a99779e2e4a7f7d81b14ea8a4eccb05487ec5d4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9321b1f2ab8808b449b317c0da9628a1ee70fe1429155c94679ad7904eea1409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.4 MB (461385036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff3ea0e6dd19cbcb2f0c0a760321ae7dcd32cbc83cb1d38041434afa54c5f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2d62050d2297db74344d3369b6ba1a7e7ae17e71f688f61f4b88c56b08e49969 NEO4J_TARBALL=neo4j-enterprise-4.4.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:19:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:19:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:19:07 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:29 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:29 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f1ead2d0e9e5e1baab7b62a2a27183133fe152824c5ec52c4a9aceda821813`  
		Last Modified: Tue, 13 Sep 2022 06:25:07 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62c4f491f69d7d8cb4ba9ab853e12f4a1d71a4ca56fbe29fb0cf55044187c42`  
		Last Modified: Tue, 13 Sep 2022 06:25:06 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ae8c3b58ef782ea410f33fe07a9de62b5decf1b567df1d9dd900df41629c9`  
		Last Modified: Tue, 13 Sep 2022 06:25:17 GMT  
		Size: 231.8 MB (231844559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:66600f0286e3b0db2f3202d951a44f27fee4bf748065d9fe2be37d7a704b68a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.6 MB (456634844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0418c71f1e407183fa23de34f33ce02f9fead82c8b83cc9d8151b08180370568`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2d62050d2297db74344d3369b6ba1a7e7ae17e71f688f61f4b88c56b08e49969 NEO4J_TARBALL=neo4j-enterprise-4.4.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:59:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:59:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:59:03 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:59:04 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:59:05 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:59:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:59:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b477b03c5968111a707b851d433689c5b3338eace827767d8a4db9151fa36bd4`  
		Last Modified: Tue, 13 Sep 2022 07:02:23 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0c756f2b19b39d7782c220796457bde5dcb5f6251ae3b63cc2170f2cf283ab`  
		Last Modified: Tue, 13 Sep 2022 07:02:23 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800af0660e6941177b5634cef2c8c2438ea31ee1364c5812dc649874f70ddcf7`  
		Last Modified: Tue, 13 Sep 2022 07:02:37 GMT  
		Size: 231.7 MB (231701331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.10`

```console
$ docker pull neo4j@sha256:e89f6b790e02bf2f1e77e9058cea7a0b5fe1038e28cce737459daaa77a9da3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.10` - linux; amd64

```console
$ docker pull neo4j@sha256:78219f2d4aaeb778686a71f346013d1af8017667bbf9c829b1f584de375b6c60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364564703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a51ce581cd34cc4ca8299fd450f7c87e757c8bb21df58f13609042e59eb2e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:19:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=869ecb89ce36fe457b4d4c4fcaa48fdf2f2d739c45323bd2c8ccdf09aa11abbf NEO4J_TARBALL=neo4j-community-4.4.10-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:19:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
# Tue, 13 Sep 2022 06:19:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:19:35 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 06:19:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:49 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:49 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173888fbd7a31f1753a1cc44f55f353927ac25c143c62dfd2f4ca3481e7742ec`  
		Last Modified: Tue, 13 Sep 2022 06:25:31 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441b1831e25394d8e002a71ed700e34b09a4f0fddf36cc283f44dd01e9c94c3e`  
		Last Modified: Tue, 13 Sep 2022 06:25:31 GMT  
		Size: 7.6 KB (7611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e178f3b6e93f63f9557249871dc76a9659464b8a695cb8705860e52690843e4`  
		Last Modified: Tue, 13 Sep 2022 06:25:38 GMT  
		Size: 135.0 MB (135024227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e5a5deed2a1cfd5e145d9ad317e71fc9fa9d87ebc51ac73c178e9e4e475945f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359813842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cba48b0d6ad8114f6cbbdb017e622928e4a73e1464036913f943e5903b1f8d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:59:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=869ecb89ce36fe457b4d4c4fcaa48fdf2f2d739c45323bd2c8ccdf09aa11abbf NEO4J_TARBALL=neo4j-community-4.4.10-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:59:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
# Tue, 13 Sep 2022 06:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:59:20 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 06:59:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:59:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:59:31 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:59:32 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:59:33 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:59:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9482fa74934e72d4fd4d4f4f320a8bc3702deeadbda70fb9432edaeb5ceaa4`  
		Last Modified: Tue, 13 Sep 2022 07:02:51 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbc277b044b5437a4f03f95be8f6fdaff82e29b73cea6578c002edc7ce61f9a`  
		Last Modified: Tue, 13 Sep 2022 07:02:51 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17210cc60647e907faf78e4314ccd975cbf0177bba639323f7eb39202589c5ce`  
		Last Modified: Tue, 13 Sep 2022 07:03:01 GMT  
		Size: 134.9 MB (134880329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.10-community`

```console
$ docker pull neo4j@sha256:e89f6b790e02bf2f1e77e9058cea7a0b5fe1038e28cce737459daaa77a9da3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.10-community` - linux; amd64

```console
$ docker pull neo4j@sha256:78219f2d4aaeb778686a71f346013d1af8017667bbf9c829b1f584de375b6c60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364564703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a51ce581cd34cc4ca8299fd450f7c87e757c8bb21df58f13609042e59eb2e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:19:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=869ecb89ce36fe457b4d4c4fcaa48fdf2f2d739c45323bd2c8ccdf09aa11abbf NEO4J_TARBALL=neo4j-community-4.4.10-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:19:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
# Tue, 13 Sep 2022 06:19:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:19:35 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 06:19:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:49 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:49 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173888fbd7a31f1753a1cc44f55f353927ac25c143c62dfd2f4ca3481e7742ec`  
		Last Modified: Tue, 13 Sep 2022 06:25:31 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441b1831e25394d8e002a71ed700e34b09a4f0fddf36cc283f44dd01e9c94c3e`  
		Last Modified: Tue, 13 Sep 2022 06:25:31 GMT  
		Size: 7.6 KB (7611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e178f3b6e93f63f9557249871dc76a9659464b8a695cb8705860e52690843e4`  
		Last Modified: Tue, 13 Sep 2022 06:25:38 GMT  
		Size: 135.0 MB (135024227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.10-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e5a5deed2a1cfd5e145d9ad317e71fc9fa9d87ebc51ac73c178e9e4e475945f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359813842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cba48b0d6ad8114f6cbbdb017e622928e4a73e1464036913f943e5903b1f8d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:59:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=869ecb89ce36fe457b4d4c4fcaa48fdf2f2d739c45323bd2c8ccdf09aa11abbf NEO4J_TARBALL=neo4j-community-4.4.10-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:59:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
# Tue, 13 Sep 2022 06:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:59:20 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 06:59:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:59:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:59:31 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:59:32 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:59:33 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:59:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9482fa74934e72d4fd4d4f4f320a8bc3702deeadbda70fb9432edaeb5ceaa4`  
		Last Modified: Tue, 13 Sep 2022 07:02:51 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbc277b044b5437a4f03f95be8f6fdaff82e29b73cea6578c002edc7ce61f9a`  
		Last Modified: Tue, 13 Sep 2022 07:02:51 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17210cc60647e907faf78e4314ccd975cbf0177bba639323f7eb39202589c5ce`  
		Last Modified: Tue, 13 Sep 2022 07:03:01 GMT  
		Size: 134.9 MB (134880329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.10-enterprise`

```console
$ docker pull neo4j@sha256:381e4a8e77e7c5b2e27a7f2e00353a1136696d6caa8b2fd1cdde305d9a25f11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.10-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:21173c726068a62590ef98883360f511fcf1ea80d73fca853bc5ea62e0e0ccc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.9 MB (460916961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e72aa9294158c8fe7c981afdacd91376dafc1df83eaff67cd85a64241eafa4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=444e8b6fd366a60fe35f868b5e3ff84509113c3fcd35d5131e07dfcce8fb9c1a NEO4J_TARBALL=neo4j-enterprise-4.4.10-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:19:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.10-unix.tar.gz
# Tue, 13 Sep 2022 06:19:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:19:55 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 06:20:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:20:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:20:17 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:20:17 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:20:17 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714a96a747c7eeff5a9ecf83a3f1a92c5ca9704b050a0ce21d6aae404b213c64`  
		Last Modified: Tue, 13 Sep 2022 06:25:48 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0384e83cbda1d3b816eec4bb163bbe4fde538819d95d60f666be8389d1321eb9`  
		Last Modified: Tue, 13 Sep 2022 06:25:48 GMT  
		Size: 7.6 KB (7611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03ad208e84cbcbbeb190f4188aea30d2f635a742ec3eb7fee9cffbc145965da`  
		Last Modified: Tue, 13 Sep 2022 06:26:00 GMT  
		Size: 231.4 MB (231376485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.10-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d31375d15fbc499eb1091d12d997dd416654ee142191d66ae846cffb643047e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.2 MB (456166380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc12c77205fb2f092c296ea99218df153021e9583af59d337216aa1f9749230`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:59:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=444e8b6fd366a60fe35f868b5e3ff84509113c3fcd35d5131e07dfcce8fb9c1a NEO4J_TARBALL=neo4j-enterprise-4.4.10-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:59:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.10-unix.tar.gz
# Tue, 13 Sep 2022 06:59:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:59:48 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 07:00:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:00:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:00:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 07:00:03 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 07:00:04 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 07:00:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 07:00:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db62eac9e8312c19128e4efcf541fb4207e1e8ac3d002b9c3ec94669adcbbd2`  
		Last Modified: Tue, 13 Sep 2022 07:03:12 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cb70f266e762532a5760db92f6d19fd5b4df55e3ffcf5f8b8a60871f01d1e8`  
		Last Modified: Tue, 13 Sep 2022 07:03:11 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778d4f870dc1cfd1cc822377c529cf3b8336bafc99da3fa7aead075c31c73d65`  
		Last Modified: Tue, 13 Sep 2022 07:03:26 GMT  
		Size: 231.2 MB (231232867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.11`

```console
$ docker pull neo4j@sha256:87458fcd5f78d9f4865a0fe26105f5051c0c80474ba99f24526e9f3544bdf31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.11` - linux; amd64

```console
$ docker pull neo4j@sha256:661f579479c8b797d0003834e79ddbfb5b9c2c3dd8217de40d9bbc93db383905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364637415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a1d9a0810a72a006a8f822ca506bca8f876fb2b88d5a34b57119d809081859`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:18:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:18:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:02 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:02 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb31dddfa2d13c70f5477d897bfef642b8bfe97f7bd883dd3f0ca3dfcb32ca0`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dc7ddb0ef7a87943a0d3ba94880718df14f33dc6634a375c688c3373c9c464`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0773aaa17b6e48fd53393008086592cc7fb670f9152f9e32b22701db3e394d50`  
		Last Modified: Tue, 13 Sep 2022 06:24:36 GMT  
		Size: 135.1 MB (135096937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.11` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9bd45fe9178fa779fcb7bc8a43b7edfd3ae1136101fefd5fe4ab45cf35445c2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359887098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f061d4eb9dbe64f565897a40424136c50b92447196498d55748f2b42005070`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:20 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:58:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:58:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:58:32 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:58:33 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:58:34 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:58:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:58:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d71b0911348d8551faffe5939c179fba47eaed5b7c8299116de7d4952697af`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80efd2fafdcbc3ae1aa49b59f7f45ab8b177bcf37d665cad020526a19449b776`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff356c782970ba7facd49528d850c914822c707df9d7146db5b63815789c9a24`  
		Last Modified: Tue, 13 Sep 2022 07:01:49 GMT  
		Size: 135.0 MB (134953583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.11-community`

```console
$ docker pull neo4j@sha256:87458fcd5f78d9f4865a0fe26105f5051c0c80474ba99f24526e9f3544bdf31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.11-community` - linux; amd64

```console
$ docker pull neo4j@sha256:661f579479c8b797d0003834e79ddbfb5b9c2c3dd8217de40d9bbc93db383905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364637415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a1d9a0810a72a006a8f822ca506bca8f876fb2b88d5a34b57119d809081859`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:18:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:18:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:02 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:02 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb31dddfa2d13c70f5477d897bfef642b8bfe97f7bd883dd3f0ca3dfcb32ca0`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dc7ddb0ef7a87943a0d3ba94880718df14f33dc6634a375c688c3373c9c464`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0773aaa17b6e48fd53393008086592cc7fb670f9152f9e32b22701db3e394d50`  
		Last Modified: Tue, 13 Sep 2022 06:24:36 GMT  
		Size: 135.1 MB (135096937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.11-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9bd45fe9178fa779fcb7bc8a43b7edfd3ae1136101fefd5fe4ab45cf35445c2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359887098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f061d4eb9dbe64f565897a40424136c50b92447196498d55748f2b42005070`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:20 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:58:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:58:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:58:32 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:58:33 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:58:34 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:58:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:58:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d71b0911348d8551faffe5939c179fba47eaed5b7c8299116de7d4952697af`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80efd2fafdcbc3ae1aa49b59f7f45ab8b177bcf37d665cad020526a19449b776`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff356c782970ba7facd49528d850c914822c707df9d7146db5b63815789c9a24`  
		Last Modified: Tue, 13 Sep 2022 07:01:49 GMT  
		Size: 135.0 MB (134953583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.11-enterprise`

```console
$ docker pull neo4j@sha256:53544639ee1fa746724b266a99779e2e4a7f7d81b14ea8a4eccb05487ec5d4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.11-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9321b1f2ab8808b449b317c0da9628a1ee70fe1429155c94679ad7904eea1409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.4 MB (461385036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff3ea0e6dd19cbcb2f0c0a760321ae7dcd32cbc83cb1d38041434afa54c5f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2d62050d2297db74344d3369b6ba1a7e7ae17e71f688f61f4b88c56b08e49969 NEO4J_TARBALL=neo4j-enterprise-4.4.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:19:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:19:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:19:07 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:29 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:29 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f1ead2d0e9e5e1baab7b62a2a27183133fe152824c5ec52c4a9aceda821813`  
		Last Modified: Tue, 13 Sep 2022 06:25:07 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62c4f491f69d7d8cb4ba9ab853e12f4a1d71a4ca56fbe29fb0cf55044187c42`  
		Last Modified: Tue, 13 Sep 2022 06:25:06 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ae8c3b58ef782ea410f33fe07a9de62b5decf1b567df1d9dd900df41629c9`  
		Last Modified: Tue, 13 Sep 2022 06:25:17 GMT  
		Size: 231.8 MB (231844559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.11-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:66600f0286e3b0db2f3202d951a44f27fee4bf748065d9fe2be37d7a704b68a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.6 MB (456634844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0418c71f1e407183fa23de34f33ce02f9fead82c8b83cc9d8151b08180370568`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2d62050d2297db74344d3369b6ba1a7e7ae17e71f688f61f4b88c56b08e49969 NEO4J_TARBALL=neo4j-enterprise-4.4.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:59:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:59:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:59:03 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:59:04 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:59:05 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:59:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:59:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b477b03c5968111a707b851d433689c5b3338eace827767d8a4db9151fa36bd4`  
		Last Modified: Tue, 13 Sep 2022 07:02:23 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0c756f2b19b39d7782c220796457bde5dcb5f6251ae3b63cc2170f2cf283ab`  
		Last Modified: Tue, 13 Sep 2022 07:02:23 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800af0660e6941177b5634cef2c8c2438ea31ee1364c5812dc649874f70ddcf7`  
		Last Modified: Tue, 13 Sep 2022 07:02:37 GMT  
		Size: 231.7 MB (231701331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.9`

```console
$ docker pull neo4j@sha256:d439b7dfafbe6d5f8956a5790ffdd02c46d8a62e3979f75acaaaad3dad8c2851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.9` - linux; amd64

```console
$ docker pull neo4j@sha256:dfb45e42ace363be182b9b104126ad114d233f361d6dd30b981efd2b44fcc8ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364372185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a200029f5f22b399acfd564f0e70400461284be117f2db81b6209603afb3ffb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4ee12a98d2dd819d6f08408429014b65264097a812ba5978c14836d6bbccb4a0 NEO4J_TARBALL=neo4j-community-4.4.9-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:20:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
# Tue, 13 Sep 2022 06:20:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:20:24 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 06:20:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:20:36 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:20:36 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:20:36 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:20:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:20:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8a36aebddfae4e0a8833cb2e3d0c0cbb9317d697e45811cbcb7cd63ab6e2a9`  
		Last Modified: Tue, 13 Sep 2022 06:26:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1357a2e98fda54f10e64dcbb94db88f7d40719f3d5e3a465dbf9de7e5a9bd68`  
		Last Modified: Tue, 13 Sep 2022 06:26:07 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110b32da9f16c739a4839d578802b860677f808c762dcd068777d82e77aa4ba`  
		Last Modified: Tue, 13 Sep 2022 06:26:14 GMT  
		Size: 134.8 MB (134831706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:38d57f99be21f2d895517b793d4ce1179449a8124454420071957e17adce7bc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.6 MB (359620587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb847c12ebb88f68d00f72b284810bf66ef06f6663b4d57b6197a195117118e2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 07:00:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4ee12a98d2dd819d6f08408429014b65264097a812ba5978c14836d6bbccb4a0 NEO4J_TARBALL=neo4j-community-4.4.9-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 07:00:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
# Tue, 13 Sep 2022 07:00:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 07:00:16 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 07:00:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:00:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:00:28 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 07:00:29 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 07:00:30 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 07:00:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 07:00:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6425b18840c019bc432204c8dd4d03b3db678f11444e3fe0e8d48663931855`  
		Last Modified: Tue, 13 Sep 2022 07:03:38 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0072c8da37b27e4eb530ebf21148cfdfddfb43c6d0aaa0634bf6cb6cd91e9924`  
		Last Modified: Tue, 13 Sep 2022 07:03:38 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7fefa31d8acd7f89cea5d0403b2d3d041cba6ce00265aa8803aaa306ea67d0`  
		Last Modified: Tue, 13 Sep 2022 07:03:47 GMT  
		Size: 134.7 MB (134687073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.9-community`

```console
$ docker pull neo4j@sha256:d439b7dfafbe6d5f8956a5790ffdd02c46d8a62e3979f75acaaaad3dad8c2851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.9-community` - linux; amd64

```console
$ docker pull neo4j@sha256:dfb45e42ace363be182b9b104126ad114d233f361d6dd30b981efd2b44fcc8ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364372185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a200029f5f22b399acfd564f0e70400461284be117f2db81b6209603afb3ffb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4ee12a98d2dd819d6f08408429014b65264097a812ba5978c14836d6bbccb4a0 NEO4J_TARBALL=neo4j-community-4.4.9-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:20:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
# Tue, 13 Sep 2022 06:20:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:20:24 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 06:20:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:20:36 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:20:36 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:20:36 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:20:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:20:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8a36aebddfae4e0a8833cb2e3d0c0cbb9317d697e45811cbcb7cd63ab6e2a9`  
		Last Modified: Tue, 13 Sep 2022 06:26:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1357a2e98fda54f10e64dcbb94db88f7d40719f3d5e3a465dbf9de7e5a9bd68`  
		Last Modified: Tue, 13 Sep 2022 06:26:07 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110b32da9f16c739a4839d578802b860677f808c762dcd068777d82e77aa4ba`  
		Last Modified: Tue, 13 Sep 2022 06:26:14 GMT  
		Size: 134.8 MB (134831706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.9-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:38d57f99be21f2d895517b793d4ce1179449a8124454420071957e17adce7bc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.6 MB (359620587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb847c12ebb88f68d00f72b284810bf66ef06f6663b4d57b6197a195117118e2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 07:00:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4ee12a98d2dd819d6f08408429014b65264097a812ba5978c14836d6bbccb4a0 NEO4J_TARBALL=neo4j-community-4.4.9-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 07:00:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
# Tue, 13 Sep 2022 07:00:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 07:00:16 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 07:00:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:00:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:00:28 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 07:00:29 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 07:00:30 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 07:00:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 07:00:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6425b18840c019bc432204c8dd4d03b3db678f11444e3fe0e8d48663931855`  
		Last Modified: Tue, 13 Sep 2022 07:03:38 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0072c8da37b27e4eb530ebf21148cfdfddfb43c6d0aaa0634bf6cb6cd91e9924`  
		Last Modified: Tue, 13 Sep 2022 07:03:38 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7fefa31d8acd7f89cea5d0403b2d3d041cba6ce00265aa8803aaa306ea67d0`  
		Last Modified: Tue, 13 Sep 2022 07:03:47 GMT  
		Size: 134.7 MB (134687073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.9-enterprise`

```console
$ docker pull neo4j@sha256:a6f8043e985e4d16e78abd7b9b7edb35fdae732292bc0eeafdec8754bfa89717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.9-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5e62131b6c627d733b4fee4ce1c734fe0b78ad297d5dd2f6b0c039c2a4a02e63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.5 MB (456549835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374afce29135a12e0117a7c2737ae4e8becae03acbe7bc22a83046034462cb19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=747b2e71b273d8f0dd82cdb594aca02b87f03f445d2ee5eaba561c8ebd474bb0 NEO4J_TARBALL=neo4j-enterprise-4.4.9-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:20:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
# Tue, 13 Sep 2022 06:20:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:20:41 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 06:21:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:21:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:21:04 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:21:04 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:21:04 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:21:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:21:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a988a508ecff0f851bb5d7aa1c549e35c61fbaaca186be4f27fb08b1883117f`  
		Last Modified: Tue, 13 Sep 2022 06:26:24 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6627036751075e19f8171f8fa8c46f23c3c02330a3e3b6c45a81295027d3a16`  
		Last Modified: Tue, 13 Sep 2022 06:26:24 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bdbb6ee4712b1ae1214894d15f2f6e859f5af86498021fc5f26f49919dcd39`  
		Last Modified: Tue, 13 Sep 2022 06:26:35 GMT  
		Size: 227.0 MB (227009359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.9-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8ce6838338a2f48e4bb9592ed7c2cb194daa4b3349054322eaf08e0fcfb58e74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.8 MB (451798867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006b34e75a971cf6285f1b97f64b8c86bffea4476f562b2aff39f7cd4cfa1f6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 07:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=747b2e71b273d8f0dd82cdb594aca02b87f03f445d2ee5eaba561c8ebd474bb0 NEO4J_TARBALL=neo4j-enterprise-4.4.9-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 07:00:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
# Tue, 13 Sep 2022 07:00:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 07:00:43 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 13 Sep 2022 07:00:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:00:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:00:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 07:01:00 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 07:01:01 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 07:01:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 07:01:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6d484f7dd60f94f30f854bbf62a0f8991ecd12295d0334b320bee2c8147df2`  
		Last Modified: Tue, 13 Sep 2022 07:03:58 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939f5f429607b785066bb0a4d99c163386528767366b8618d5c16f0c1d72638`  
		Last Modified: Tue, 13 Sep 2022 07:03:57 GMT  
		Size: 7.6 KB (7586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbbd36a098187129b45188c35ea6cfb4bed7e42f44e44f6b97373a7144ae178`  
		Last Modified: Tue, 13 Sep 2022 07:04:12 GMT  
		Size: 226.9 MB (226865352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:87458fcd5f78d9f4865a0fe26105f5051c0c80474ba99f24526e9f3544bdf31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:661f579479c8b797d0003834e79ddbfb5b9c2c3dd8217de40d9bbc93db383905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364637415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a1d9a0810a72a006a8f822ca506bca8f876fb2b88d5a34b57119d809081859`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:18:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:18:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:02 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:02 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb31dddfa2d13c70f5477d897bfef642b8bfe97f7bd883dd3f0ca3dfcb32ca0`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dc7ddb0ef7a87943a0d3ba94880718df14f33dc6634a375c688c3373c9c464`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0773aaa17b6e48fd53393008086592cc7fb670f9152f9e32b22701db3e394d50`  
		Last Modified: Tue, 13 Sep 2022 06:24:36 GMT  
		Size: 135.1 MB (135096937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9bd45fe9178fa779fcb7bc8a43b7edfd3ae1136101fefd5fe4ab45cf35445c2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359887098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f061d4eb9dbe64f565897a40424136c50b92447196498d55748f2b42005070`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:20 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:58:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:58:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:58:32 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:58:33 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:58:34 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:58:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:58:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d71b0911348d8551faffe5939c179fba47eaed5b7c8299116de7d4952697af`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80efd2fafdcbc3ae1aa49b59f7f45ab8b177bcf37d665cad020526a19449b776`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff356c782970ba7facd49528d850c914822c707df9d7146db5b63815789c9a24`  
		Last Modified: Tue, 13 Sep 2022 07:01:49 GMT  
		Size: 135.0 MB (134953583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:53544639ee1fa746724b266a99779e2e4a7f7d81b14ea8a4eccb05487ec5d4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9321b1f2ab8808b449b317c0da9628a1ee70fe1429155c94679ad7904eea1409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.4 MB (461385036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff3ea0e6dd19cbcb2f0c0a760321ae7dcd32cbc83cb1d38041434afa54c5f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2d62050d2297db74344d3369b6ba1a7e7ae17e71f688f61f4b88c56b08e49969 NEO4J_TARBALL=neo4j-enterprise-4.4.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:19:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:19:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:19:07 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:29 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:29 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f1ead2d0e9e5e1baab7b62a2a27183133fe152824c5ec52c4a9aceda821813`  
		Last Modified: Tue, 13 Sep 2022 06:25:07 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62c4f491f69d7d8cb4ba9ab853e12f4a1d71a4ca56fbe29fb0cf55044187c42`  
		Last Modified: Tue, 13 Sep 2022 06:25:06 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ae8c3b58ef782ea410f33fe07a9de62b5decf1b567df1d9dd900df41629c9`  
		Last Modified: Tue, 13 Sep 2022 06:25:17 GMT  
		Size: 231.8 MB (231844559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:66600f0286e3b0db2f3202d951a44f27fee4bf748065d9fe2be37d7a704b68a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.6 MB (456634844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0418c71f1e407183fa23de34f33ce02f9fead82c8b83cc9d8151b08180370568`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2d62050d2297db74344d3369b6ba1a7e7ae17e71f688f61f4b88c56b08e49969 NEO4J_TARBALL=neo4j-enterprise-4.4.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:59:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:59:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:59:03 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:59:04 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:59:05 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:59:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:59:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b477b03c5968111a707b851d433689c5b3338eace827767d8a4db9151fa36bd4`  
		Last Modified: Tue, 13 Sep 2022 07:02:23 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0c756f2b19b39d7782c220796457bde5dcb5f6251ae3b63cc2170f2cf283ab`  
		Last Modified: Tue, 13 Sep 2022 07:02:23 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800af0660e6941177b5634cef2c8c2438ea31ee1364c5812dc649874f70ddcf7`  
		Last Modified: Tue, 13 Sep 2022 07:02:37 GMT  
		Size: 231.7 MB (231701331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:87458fcd5f78d9f4865a0fe26105f5051c0c80474ba99f24526e9f3544bdf31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:661f579479c8b797d0003834e79ddbfb5b9c2c3dd8217de40d9bbc93db383905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364637415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a1d9a0810a72a006a8f822ca506bca8f876fb2b88d5a34b57119d809081859`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:18:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:18:45 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:18:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:18:48 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:19:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:19:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:19:02 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:19:02 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:19:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:19:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a2774ad4f184f0a10c74dd66c9b4fdf76a60a8dbb311b9499b3173aabfcc61`  
		Last Modified: Tue, 13 Sep 2022 06:24:44 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb31dddfa2d13c70f5477d897bfef642b8bfe97f7bd883dd3f0ca3dfcb32ca0`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dc7ddb0ef7a87943a0d3ba94880718df14f33dc6634a375c688c3373c9c464`  
		Last Modified: Tue, 13 Sep 2022 06:24:29 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0773aaa17b6e48fd53393008086592cc7fb670f9152f9e32b22701db3e394d50`  
		Last Modified: Tue, 13 Sep 2022 06:24:36 GMT  
		Size: 135.1 MB (135096937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9bd45fe9178fa779fcb7bc8a43b7edfd3ae1136101fefd5fe4ab45cf35445c2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359887098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f061d4eb9dbe64f565897a40424136c50b92447196498d55748f2b42005070`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Sep 2022 06:58:16 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Tue, 13 Sep 2022 06:58:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=28810daac5de4a5d5b77ce2da7d7c3da4c5ccf13288bad885b833c35b96100c8 NEO4J_TARBALL=neo4j-community-4.4.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Sep 2022 06:58:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
# Tue, 13 Sep 2022 06:58:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Sep 2022 06:58:20 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Tue, 13 Sep 2022 06:58:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:58:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:58:32 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Sep 2022 06:58:33 GMT
VOLUME [/data /logs]
# Tue, 13 Sep 2022 06:58:34 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Sep 2022 06:58:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 06:58:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4184f46e59fa544d67090bc1b94d36f2af8c4757717aecdc90e0819aadac9`  
		Last Modified: Tue, 13 Sep 2022 07:01:59 GMT  
		Size: 194.9 MB (194867856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d71b0911348d8551faffe5939c179fba47eaed5b7c8299116de7d4952697af`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80efd2fafdcbc3ae1aa49b59f7f45ab8b177bcf37d665cad020526a19449b776`  
		Last Modified: Tue, 13 Sep 2022 07:01:40 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff356c782970ba7facd49528d850c914822c707df9d7146db5b63815789c9a24`  
		Last Modified: Tue, 13 Sep 2022 07:01:49 GMT  
		Size: 135.0 MB (134953583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
