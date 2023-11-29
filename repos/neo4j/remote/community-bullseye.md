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
