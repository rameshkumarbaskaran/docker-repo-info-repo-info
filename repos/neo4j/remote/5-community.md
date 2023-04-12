## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:b817478d92e2bc20dba98742f40927c8988ec0a090be38cc096ba6222bd16041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:0a8ed3602875ffe0807e0e4046663763ec481a260e12ada91b3fcbd23dec0e89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339542637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2bbb766df78905a61eb61755bcadc15acb4ae15280029d78410afdc74acec8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:16:43 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:27:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:27:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 08:27:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:27:37 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 08:27:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:27:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:27:48 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:27:48 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:27:48 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:27:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:27:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddd9ea3ca0dd85f3af3e4aaaa2acdd08b9f289fab659372eedc7fd033de543c`  
		Last Modified: Wed, 12 Apr 2023 08:24:58 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2468aaaf0a78abc2d5737b5b48245f7d54294ae4dabd1b4e6e3bb3d5ee24a0a`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa783c941a481477b08af1f779e1909cdb32dda1fd6d257bb32e7157f8388963`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 8.6 KB (8627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081b9e3f57b27f4f7d7cd842c6abaf737f0ee52f50d3b2fda0c7097c70762436`  
		Last Modified: Wed, 12 Apr 2023 08:29:01 GMT  
		Size: 115.7 MB (115673660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b338729acc57a8b23e3f07dde6ee307fea7bc848c5c85c3ef35c7c03fa2a10ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336868264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a478ab5d3a4dd7a7b0bc781f8c3ef96e4b8799ade7c896bf2a003d2f589e44f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:23:36 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 04:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 04:19:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:05 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:05 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:05 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9701f65253cb8cdaa00fd933b855a5c7977f66e7e7b1e8cfa93ad00f587f6479`  
		Last Modified: Wed, 12 Apr 2023 01:31:17 GMT  
		Size: 191.3 MB (191260431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35efb11ab5fe742be81e3c2049cb3053ff82a73d15963bbd20c405948c1338e7`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701ed5e8b2fbc8c1b8d5c7b7b8a70d83a750d2e30b318198f675edccd62024a8`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 8.6 KB (8631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ca08505b7f879ec6594895fc709ae06d279848756db5c3ea85dc7ff90b6bf3`  
		Last Modified: Wed, 12 Apr 2023 04:20:18 GMT  
		Size: 115.5 MB (115531491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
