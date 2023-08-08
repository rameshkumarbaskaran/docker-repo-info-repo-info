## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:98057ba9ff553af1b613b77563073a8fc0da22543929094d4892ff11a4b54f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5874e47a9379a1240b3f882ea7fc95e4280f9fd7184e644f36fe20ea59dae836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046b56c921a92d488b320b83d195fa8b5349ebbcbdb5c97f08986577737168fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Aug 2023 20:17:57 GMT
COPY dir:8ea3eea47bd8b9d37ce2403b2d64b2cdc0fec836a119c10ec3e4ff0bcca8bb4d in /opt/java/openjdk 
# Tue, 08 Aug 2023 20:17:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 08 Aug 2023 20:17:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Tue, 08 Aug 2023 20:17:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 08 Aug 2023 20:17:59 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 08 Aug 2023 20:18:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 20:18:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 20:18:12 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Aug 2023 20:18:12 GMT
VOLUME [/data /logs]
# Tue, 08 Aug 2023 20:18:12 GMT
EXPOSE 7473 7474 7687
# Tue, 08 Aug 2023 20:18:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Aug 2023 20:18:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8050892377b9a47e9c3a9ef290967338da628f34d31341e0efc181a16a685401`  
		Last Modified: Tue, 08 Aug 2023 20:20:46 GMT  
		Size: 144.8 MB (144773775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75da6703eab987e8984f55f7b119d2a52024789a03b0018da5bc08444016fe31`  
		Last Modified: Tue, 08 Aug 2023 20:20:35 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5922df7beb8fe619290607acbbd9e2aa1afb897780a263c3145811da143518`  
		Last Modified: Tue, 08 Aug 2023 20:20:35 GMT  
		Size: 9.3 KB (9348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33ae22e818e7af68ff2908b8acb8840130f0d5d9a7c28663a6e611f55cba1a4`  
		Last Modified: Tue, 08 Aug 2023 20:20:43 GMT  
		Size: 117.5 MB (117490229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5eff050db886fd158c70403db386fd8197713d8a9ff4a7169e95f327052fd2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290998058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10f118eda1f398b70a20d9654b2c32311223d8bec148a4199ee5a6ca6385061`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:25:26 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 14:25:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 14:25:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 14:25:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 14:25:31 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 14:25:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:25:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:25:42 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 14:25:42 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 14:25:42 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 14:25:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:25:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc8dfc50ad1a93c8652ce31df19291350dca86cc2b7462fbd67c78d39e53aca`  
		Last Modified: Fri, 28 Jul 2023 14:27:39 GMT  
		Size: 143.5 MB (143538104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09154e394cdcafd707756229b7f59b9278dad9c9b82bc55c959ce96cea555cca`  
		Last Modified: Fri, 28 Jul 2023 14:27:30 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0073dc53bf752a406b1f1a9466f1852d2406bc935170d0ddc9995ac39ba207cb`  
		Last Modified: Fri, 28 Jul 2023 14:27:30 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bc67fb0551713c2e37231017c636ef2bde5a234bb6de3037c4fec4ee6bcd1b`  
		Last Modified: Fri, 28 Jul 2023 14:27:38 GMT  
		Size: 117.4 MB (117383884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
