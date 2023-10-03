## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:98858e8c66dcf9229c8a46d778947929ab396a6c8659c5773e77399bf85610a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:c8a1b54973cf0aea0101e334f24252bc61e2737ed24a05c30f75f2d599a59746
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292665338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e811f23adee2d6508a50f57ef0561233ad9d208069a1b7797d38925440957a0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:44:13 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Tue, 03 Oct 2023 10:09:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=adf9e7915f5c10dfa4daf9eab79852660887eac3c3e165741fce48415c0b6f34 NEO4J_TARBALL=neo4j-community-5.12.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 03 Oct 2023 10:09:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
# Tue, 03 Oct 2023 10:09:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 03 Oct 2023 10:09:25 GMT
COPY multi:f4e8828c26bc3c80f7c5af331adb809a61a5b929b6f67c8cd774aa23152e75a5 in /startup/ 
# Tue, 03 Oct 2023 10:09:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 10:09:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 10:09:39 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Oct 2023 10:09:39 GMT
VOLUME [/data /logs]
# Tue, 03 Oct 2023 10:09:39 GMT
EXPOSE 7473 7474 7687
# Tue, 03 Oct 2023 10:09:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Oct 2023 10:09:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0567cd6aa99e5db3b54cc244cfee493561efcb8009ca2dc2c87b8c882d0bd562`  
		Last Modified: Tue, 03 Oct 2023 08:56:51 GMT  
		Size: 144.8 MB (144775742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b91728bb38c426ddf3cafcf732ab5fd167e18ebf3cafe8596748b5a3b477cd6`  
		Last Modified: Tue, 03 Oct 2023 10:11:48 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc4040aa0a7249238542f14d051dac83d721a18e99e698abc199b39d9d23b45`  
		Last Modified: Tue, 03 Oct 2023 10:11:48 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e35e2e7b5b30f3cb6a905a95bb6da9d029eebd315e963dfd4e7c1c1b6b1751`  
		Last Modified: Tue, 03 Oct 2023 10:11:54 GMT  
		Size: 116.5 MB (116458587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3e3f90281fcd4a2aa65ccdb2d917da279c5ea984160e64df33add4a186d7acf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289971161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5241c98d493129a869aa26df6a780ef653a1bf31385d77b0726049b092713872`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:48:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:32:36 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Tue, 03 Oct 2023 09:03:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=adf9e7915f5c10dfa4daf9eab79852660887eac3c3e165741fce48415c0b6f34 NEO4J_TARBALL=neo4j-community-5.12.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 03 Oct 2023 09:03:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
# Tue, 03 Oct 2023 09:03:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 03 Oct 2023 09:03:24 GMT
COPY multi:f4e8828c26bc3c80f7c5af331adb809a61a5b929b6f67c8cd774aa23152e75a5 in /startup/ 
# Tue, 03 Oct 2023 09:03:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 09:03:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 09:03:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Oct 2023 09:03:35 GMT
VOLUME [/data /logs]
# Tue, 03 Oct 2023 09:03:35 GMT
EXPOSE 7473 7474 7687
# Tue, 03 Oct 2023 09:03:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Oct 2023 09:03:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0f8e5bf90a9369ab6f51e945ac866f2ec10afab1f1331f92ddd272ac850a21`  
		Last Modified: Tue, 03 Oct 2023 08:41:12 GMT  
		Size: 143.5 MB (143543520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6959367bc3458dcf2703a81e2d962bd01b1285049325b05b0072aee98d36eea`  
		Last Modified: Tue, 03 Oct 2023 09:05:48 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136359f3b5e932e45e1fe79eca645b1cebf2e9409d148063f94563942383d67d`  
		Last Modified: Tue, 03 Oct 2023 09:05:48 GMT  
		Size: 9.4 KB (9428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4eb39256e4fc4c53601a76a6ceb66eb7b98c5b52b648f730c3b0f0393f94236`  
		Last Modified: Tue, 03 Oct 2023 09:05:54 GMT  
		Size: 116.4 MB (116351457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
