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
