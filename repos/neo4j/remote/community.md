## `neo4j:community`

```console
$ docker pull neo4j@sha256:cb74d205fabb0acee594d8cd6d8433a6248b9a92d03778b66907dd4c93aca085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa9ed6ececd003c4ea80104b4b200150141f34303cff74ee1289988a57e8f30d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f75bff79bbe533a724921207f5c0febacdeae83841e95e8b8ac5830b80e66`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:08:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:08:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:08:41 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:08:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:08:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:08:57 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:08:57 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:08:57 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:08:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:08:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e001ddc63a4f7b55f811d3d54e0f5bebb86d5485219d94c03d9916f4d5617bfe`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c518db23e44a7853b593eec4a067cb1dac9637d76493e511e5f563c9e2b085`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dc49f41a37e67e5f40aeccfb78ee248cefb4943e39cca13d1eb7ddaceab6c`  
		Last Modified: Thu, 16 Mar 2023 07:10:30 GMT  
		Size: 115.2 MB (115196191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2af3cc70a0f6e5db6a53a824dbb3718455ceaa8c1efcbc63aa32e07b9cb98f95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a61e5dff5f0a1c529d748067a99917f41b3eccbb48d83863574d3b0cb6fbea`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:52:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 Mar 2023 06:57:23 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 23 Mar 2023 09:27:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 Mar 2023 09:27:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 23 Mar 2023 09:27:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 23 Mar 2023 09:27:15 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 23 Mar 2023 09:27:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:27:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 09:27:26 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 Mar 2023 09:27:26 GMT
VOLUME [/data /logs]
# Thu, 23 Mar 2023 09:27:26 GMT
EXPOSE 7473 7474 7687
# Thu, 23 Mar 2023 09:27:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 Mar 2023 09:27:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce46c3fded23542cb5a993d929bb8b2dfc32a31d4c9928588d2da3bc91d84fec`  
		Last Modified: Thu, 23 Mar 2023 07:06:00 GMT  
		Size: 191.3 MB (191260416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ea444f3fd75be0280d291748149cffc995d040f33189e7bc23a9ff1bf5a5cf`  
		Last Modified: Thu, 23 Mar 2023 09:28:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001173b42e9f4e22d73ea2aa68675a9d05626f266364b011756e97ab0454a348`  
		Last Modified: Thu, 23 Mar 2023 09:28:41 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd45512fbe455568a26f25fca1d06bb9a93189e9ee9ec098114740f81e01cf`  
		Last Modified: Thu, 23 Mar 2023 09:28:46 GMT  
		Size: 115.1 MB (115051256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
