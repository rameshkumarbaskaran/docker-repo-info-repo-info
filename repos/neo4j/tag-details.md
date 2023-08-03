<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.24`](#neo4j4424)
-	[`neo4j:4.4.24-community`](#neo4j4424-community)
-	[`neo4j:4.4.24-enterprise`](#neo4j4424-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.10`](#neo4j510)
-	[`neo4j:5.10-bullseye`](#neo4j510-bullseye)
-	[`neo4j:5.10-community`](#neo4j510-community)
-	[`neo4j:5.10-community-bullseye`](#neo4j510-community-bullseye)
-	[`neo4j:5.10-community-ubi8`](#neo4j510-community-ubi8)
-	[`neo4j:5.10-enterprise`](#neo4j510-enterprise)
-	[`neo4j:5.10-enterprise-bullseye`](#neo4j510-enterprise-bullseye)
-	[`neo4j:5.10-enterprise-ubi8`](#neo4j510-enterprise-ubi8)
-	[`neo4j:5.10-ubi8`](#neo4j510-ubi8)
-	[`neo4j:5.10.0`](#neo4j5100)
-	[`neo4j:5.10.0-bullseye`](#neo4j5100-bullseye)
-	[`neo4j:5.10.0-community`](#neo4j5100-community)
-	[`neo4j:5.10.0-community-bullseye`](#neo4j5100-community-bullseye)
-	[`neo4j:5.10.0-community-ubi8`](#neo4j5100-community-ubi8)
-	[`neo4j:5.10.0-enterprise`](#neo4j5100-enterprise)
-	[`neo4j:5.10.0-enterprise-bullseye`](#neo4j5100-enterprise-bullseye)
-	[`neo4j:5.10.0-enterprise-ubi8`](#neo4j5100-enterprise-ubi8)
-	[`neo4j:5.10.0-ubi8`](#neo4j5100-ubi8)
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
$ docker pull neo4j@sha256:769310b01b016579a7e6fd6567eb05dcaa14acfb75947013c5b129d835504055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:db0243ebe391dd9270adcc00dd1fc1709198eedf0007f68a6a2004fe8cea63f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298547747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa7ab73f0682068bba11a02bfa87ddc0a69b4f560949cbccf825f7c22683b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:57 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Thu, 03 Aug 2023 22:20:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2e76f3d237648392c9fb43b6a93fbd30cb00da617a30d13712b386a69565e43a NEO4J_TARBALL=neo4j-community-4.4.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 22:20:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 22:20:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 22:20:02 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 22:20:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 22:20:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 22:20:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 22:20:16 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 22:20:16 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 22:20:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 22:20:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8093463543ce0d2e4cc72a5011db04a63e89f8a49c37702622adc8e1defc155b`  
		Last Modified: Fri, 28 Jul 2023 02:25:48 GMT  
		Size: 144.8 MB (144829555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608d42a4f0540314ed46f339bac1e8932c803de195109c909b435b7a11f45ae1`  
		Last Modified: Thu, 03 Aug 2023 22:21:15 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f07126d07e2094f242328d2cd712a019de44d40983319c42bc3eb6f65a57d2`  
		Last Modified: Thu, 03 Aug 2023 22:21:15 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d47b3c73dfb4db7023351d7a6165c578fe9237a1004d192f1327c696a792b86`  
		Last Modified: Thu, 03 Aug 2023 22:21:26 GMT  
		Size: 122.3 MB (122287405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:65386caf28ba5f274f106ffe2ee596a25112d411053b97e1ea160183e5f45732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293820257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370310b59b76d97e6702bcb1650021f153a76ea58ca0e74de2912765c3992ec1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:26:26 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Thu, 03 Aug 2023 21:40:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2e76f3d237648392c9fb43b6a93fbd30cb00da617a30d13712b386a69565e43a NEO4J_TARBALL=neo4j-community-4.4.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 21:40:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 21:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 21:40:32 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 21:40:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 21:40:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 21:40:44 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 21:40:44 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 21:40:44 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 21:40:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:40:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f2de644281932f812dc6760827991ae5ed5aba2a3bc3c4f617f109f75f6b20`  
		Last Modified: Fri, 28 Jul 2023 14:29:12 GMT  
		Size: 141.6 MB (141565323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291f74ef2027169417bffc8514985b859e252aea8f68deddd4a510cb293c9d31`  
		Last Modified: Thu, 03 Aug 2023 21:41:43 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111770706db2ee98bc3258bf02aef2060d250e36e054e9fa243951856cd9df7`  
		Last Modified: Thu, 03 Aug 2023 21:41:44 GMT  
		Size: 9.3 KB (9328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe90dadc8b31d675934cefac8762ed59c9d06d31b4ee4541cadf0aa05930988`  
		Last Modified: Thu, 03 Aug 2023 21:41:50 GMT  
		Size: 122.2 MB (122178886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:769310b01b016579a7e6fd6567eb05dcaa14acfb75947013c5b129d835504055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:db0243ebe391dd9270adcc00dd1fc1709198eedf0007f68a6a2004fe8cea63f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298547747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa7ab73f0682068bba11a02bfa87ddc0a69b4f560949cbccf825f7c22683b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:57 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Thu, 03 Aug 2023 22:20:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2e76f3d237648392c9fb43b6a93fbd30cb00da617a30d13712b386a69565e43a NEO4J_TARBALL=neo4j-community-4.4.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 22:20:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 22:20:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 22:20:02 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 22:20:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 22:20:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 22:20:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 22:20:16 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 22:20:16 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 22:20:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 22:20:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8093463543ce0d2e4cc72a5011db04a63e89f8a49c37702622adc8e1defc155b`  
		Last Modified: Fri, 28 Jul 2023 02:25:48 GMT  
		Size: 144.8 MB (144829555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608d42a4f0540314ed46f339bac1e8932c803de195109c909b435b7a11f45ae1`  
		Last Modified: Thu, 03 Aug 2023 22:21:15 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f07126d07e2094f242328d2cd712a019de44d40983319c42bc3eb6f65a57d2`  
		Last Modified: Thu, 03 Aug 2023 22:21:15 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d47b3c73dfb4db7023351d7a6165c578fe9237a1004d192f1327c696a792b86`  
		Last Modified: Thu, 03 Aug 2023 22:21:26 GMT  
		Size: 122.3 MB (122287405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:65386caf28ba5f274f106ffe2ee596a25112d411053b97e1ea160183e5f45732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293820257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370310b59b76d97e6702bcb1650021f153a76ea58ca0e74de2912765c3992ec1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:26:26 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Thu, 03 Aug 2023 21:40:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2e76f3d237648392c9fb43b6a93fbd30cb00da617a30d13712b386a69565e43a NEO4J_TARBALL=neo4j-community-4.4.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 21:40:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 21:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 21:40:32 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 21:40:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 21:40:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 21:40:44 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 21:40:44 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 21:40:44 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 21:40:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:40:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f2de644281932f812dc6760827991ae5ed5aba2a3bc3c4f617f109f75f6b20`  
		Last Modified: Fri, 28 Jul 2023 14:29:12 GMT  
		Size: 141.6 MB (141565323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291f74ef2027169417bffc8514985b859e252aea8f68deddd4a510cb293c9d31`  
		Last Modified: Thu, 03 Aug 2023 21:41:43 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111770706db2ee98bc3258bf02aef2060d250e36e054e9fa243951856cd9df7`  
		Last Modified: Thu, 03 Aug 2023 21:41:44 GMT  
		Size: 9.3 KB (9328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe90dadc8b31d675934cefac8762ed59c9d06d31b4ee4541cadf0aa05930988`  
		Last Modified: Thu, 03 Aug 2023 21:41:50 GMT  
		Size: 122.2 MB (122178886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:86364ec1a4c91fbc73d5ea83e31d73d89a00244282693e4672384eb156a96f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9adab1ad966e2f109aab99bf17a54698fd32a2d7d36389e1f26d765cc85ba69b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (398012023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6728218fa181903474ce54a3bee36084020b0f7d59784ad0e06cb9fd275ad1f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:57 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Thu, 03 Aug 2023 22:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f1b4862dd7312590036d9167eb0120df62b792522ef2e567a59549bfad880cca NEO4J_TARBALL=neo4j-enterprise-4.4.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 22:20:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 22:20:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 22:20:23 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 22:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 22:20:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 22:20:37 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 22:20:37 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 22:20:37 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 22:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 22:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8093463543ce0d2e4cc72a5011db04a63e89f8a49c37702622adc8e1defc155b`  
		Last Modified: Fri, 28 Jul 2023 02:25:48 GMT  
		Size: 144.8 MB (144829555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ebff276b33a6474f88135f9ef6dca5875fbee81fafa338946bc325ec7c5b30`  
		Last Modified: Thu, 03 Aug 2023 22:21:39 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba481ffc2da2424ee071164c437d4adc366efe7f79a479ec80123570b26eb2e3`  
		Last Modified: Thu, 03 Aug 2023 22:21:39 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2080449f6aaec6b003a09cc9ec054aefc7ea354e4ec6178127830b767bdf53ca`  
		Last Modified: Thu, 03 Aug 2023 22:21:50 GMT  
		Size: 221.8 MB (221751679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a16e76ecef53d17edf5703cbfa933b8d562e1a367bbaaa19060f5fa047f827a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.3 MB (393285193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ddeb4288570f691a68fe4aa2ab8882b36746f34a3fd76cb63c5fe96b95378c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:26:26 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Thu, 03 Aug 2023 21:40:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f1b4862dd7312590036d9167eb0120df62b792522ef2e567a59549bfad880cca NEO4J_TARBALL=neo4j-enterprise-4.4.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 21:40:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 21:40:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 21:40:48 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 21:41:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 21:41:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 21:41:07 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 21:41:08 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 21:41:08 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 21:41:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:41:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f2de644281932f812dc6760827991ae5ed5aba2a3bc3c4f617f109f75f6b20`  
		Last Modified: Fri, 28 Jul 2023 14:29:12 GMT  
		Size: 141.6 MB (141565323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7250bd21ad398820f23a94dcd2eba7e4f43ca58d419ff96ea286c9e039af6dc9`  
		Last Modified: Thu, 03 Aug 2023 21:42:03 GMT  
		Size: 3.9 KB (3896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832b529f2810befbd8c1bb109b32c7457705482ec1efbbf636150ca7b3497b38`  
		Last Modified: Thu, 03 Aug 2023 21:42:03 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e6f3839812e504e4f913404e830558119e6f170196c32efbf37ff497cc9134`  
		Last Modified: Thu, 03 Aug 2023 21:42:18 GMT  
		Size: 221.6 MB (221643816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.24`

```console
$ docker pull neo4j@sha256:769310b01b016579a7e6fd6567eb05dcaa14acfb75947013c5b129d835504055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.24` - linux; amd64

```console
$ docker pull neo4j@sha256:db0243ebe391dd9270adcc00dd1fc1709198eedf0007f68a6a2004fe8cea63f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298547747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa7ab73f0682068bba11a02bfa87ddc0a69b4f560949cbccf825f7c22683b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:57 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Thu, 03 Aug 2023 22:20:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2e76f3d237648392c9fb43b6a93fbd30cb00da617a30d13712b386a69565e43a NEO4J_TARBALL=neo4j-community-4.4.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 22:20:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 22:20:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 22:20:02 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 22:20:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 22:20:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 22:20:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 22:20:16 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 22:20:16 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 22:20:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 22:20:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8093463543ce0d2e4cc72a5011db04a63e89f8a49c37702622adc8e1defc155b`  
		Last Modified: Fri, 28 Jul 2023 02:25:48 GMT  
		Size: 144.8 MB (144829555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608d42a4f0540314ed46f339bac1e8932c803de195109c909b435b7a11f45ae1`  
		Last Modified: Thu, 03 Aug 2023 22:21:15 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f07126d07e2094f242328d2cd712a019de44d40983319c42bc3eb6f65a57d2`  
		Last Modified: Thu, 03 Aug 2023 22:21:15 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d47b3c73dfb4db7023351d7a6165c578fe9237a1004d192f1327c696a792b86`  
		Last Modified: Thu, 03 Aug 2023 22:21:26 GMT  
		Size: 122.3 MB (122287405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.24` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:65386caf28ba5f274f106ffe2ee596a25112d411053b97e1ea160183e5f45732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293820257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370310b59b76d97e6702bcb1650021f153a76ea58ca0e74de2912765c3992ec1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:26:26 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Thu, 03 Aug 2023 21:40:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2e76f3d237648392c9fb43b6a93fbd30cb00da617a30d13712b386a69565e43a NEO4J_TARBALL=neo4j-community-4.4.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 21:40:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 21:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 21:40:32 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 21:40:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 21:40:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 21:40:44 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 21:40:44 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 21:40:44 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 21:40:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:40:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f2de644281932f812dc6760827991ae5ed5aba2a3bc3c4f617f109f75f6b20`  
		Last Modified: Fri, 28 Jul 2023 14:29:12 GMT  
		Size: 141.6 MB (141565323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291f74ef2027169417bffc8514985b859e252aea8f68deddd4a510cb293c9d31`  
		Last Modified: Thu, 03 Aug 2023 21:41:43 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111770706db2ee98bc3258bf02aef2060d250e36e054e9fa243951856cd9df7`  
		Last Modified: Thu, 03 Aug 2023 21:41:44 GMT  
		Size: 9.3 KB (9328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe90dadc8b31d675934cefac8762ed59c9d06d31b4ee4541cadf0aa05930988`  
		Last Modified: Thu, 03 Aug 2023 21:41:50 GMT  
		Size: 122.2 MB (122178886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.24-community`

```console
$ docker pull neo4j@sha256:769310b01b016579a7e6fd6567eb05dcaa14acfb75947013c5b129d835504055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.24-community` - linux; amd64

```console
$ docker pull neo4j@sha256:db0243ebe391dd9270adcc00dd1fc1709198eedf0007f68a6a2004fe8cea63f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298547747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa7ab73f0682068bba11a02bfa87ddc0a69b4f560949cbccf825f7c22683b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:57 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Thu, 03 Aug 2023 22:20:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2e76f3d237648392c9fb43b6a93fbd30cb00da617a30d13712b386a69565e43a NEO4J_TARBALL=neo4j-community-4.4.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 22:20:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 22:20:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 22:20:02 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 22:20:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 22:20:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 22:20:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 22:20:16 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 22:20:16 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 22:20:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 22:20:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8093463543ce0d2e4cc72a5011db04a63e89f8a49c37702622adc8e1defc155b`  
		Last Modified: Fri, 28 Jul 2023 02:25:48 GMT  
		Size: 144.8 MB (144829555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608d42a4f0540314ed46f339bac1e8932c803de195109c909b435b7a11f45ae1`  
		Last Modified: Thu, 03 Aug 2023 22:21:15 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f07126d07e2094f242328d2cd712a019de44d40983319c42bc3eb6f65a57d2`  
		Last Modified: Thu, 03 Aug 2023 22:21:15 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d47b3c73dfb4db7023351d7a6165c578fe9237a1004d192f1327c696a792b86`  
		Last Modified: Thu, 03 Aug 2023 22:21:26 GMT  
		Size: 122.3 MB (122287405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.24-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:65386caf28ba5f274f106ffe2ee596a25112d411053b97e1ea160183e5f45732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293820257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370310b59b76d97e6702bcb1650021f153a76ea58ca0e74de2912765c3992ec1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:26:26 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Thu, 03 Aug 2023 21:40:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2e76f3d237648392c9fb43b6a93fbd30cb00da617a30d13712b386a69565e43a NEO4J_TARBALL=neo4j-community-4.4.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 21:40:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 21:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 21:40:32 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 21:40:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 21:40:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 21:40:44 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 21:40:44 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 21:40:44 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 21:40:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:40:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f2de644281932f812dc6760827991ae5ed5aba2a3bc3c4f617f109f75f6b20`  
		Last Modified: Fri, 28 Jul 2023 14:29:12 GMT  
		Size: 141.6 MB (141565323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291f74ef2027169417bffc8514985b859e252aea8f68deddd4a510cb293c9d31`  
		Last Modified: Thu, 03 Aug 2023 21:41:43 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111770706db2ee98bc3258bf02aef2060d250e36e054e9fa243951856cd9df7`  
		Last Modified: Thu, 03 Aug 2023 21:41:44 GMT  
		Size: 9.3 KB (9328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe90dadc8b31d675934cefac8762ed59c9d06d31b4ee4541cadf0aa05930988`  
		Last Modified: Thu, 03 Aug 2023 21:41:50 GMT  
		Size: 122.2 MB (122178886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.24-enterprise`

```console
$ docker pull neo4j@sha256:86364ec1a4c91fbc73d5ea83e31d73d89a00244282693e4672384eb156a96f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.24-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9adab1ad966e2f109aab99bf17a54698fd32a2d7d36389e1f26d765cc85ba69b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (398012023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6728218fa181903474ce54a3bee36084020b0f7d59784ad0e06cb9fd275ad1f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:57 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Thu, 03 Aug 2023 22:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f1b4862dd7312590036d9167eb0120df62b792522ef2e567a59549bfad880cca NEO4J_TARBALL=neo4j-enterprise-4.4.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 22:20:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 22:20:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 22:20:23 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 22:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 22:20:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 22:20:37 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 22:20:37 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 22:20:37 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 22:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 22:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8093463543ce0d2e4cc72a5011db04a63e89f8a49c37702622adc8e1defc155b`  
		Last Modified: Fri, 28 Jul 2023 02:25:48 GMT  
		Size: 144.8 MB (144829555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ebff276b33a6474f88135f9ef6dca5875fbee81fafa338946bc325ec7c5b30`  
		Last Modified: Thu, 03 Aug 2023 22:21:39 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba481ffc2da2424ee071164c437d4adc366efe7f79a479ec80123570b26eb2e3`  
		Last Modified: Thu, 03 Aug 2023 22:21:39 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2080449f6aaec6b003a09cc9ec054aefc7ea354e4ec6178127830b767bdf53ca`  
		Last Modified: Thu, 03 Aug 2023 22:21:50 GMT  
		Size: 221.8 MB (221751679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.24-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a16e76ecef53d17edf5703cbfa933b8d562e1a367bbaaa19060f5fa047f827a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.3 MB (393285193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ddeb4288570f691a68fe4aa2ab8882b36746f34a3fd76cb63c5fe96b95378c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:26:26 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Thu, 03 Aug 2023 21:40:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f1b4862dd7312590036d9167eb0120df62b792522ef2e567a59549bfad880cca NEO4J_TARBALL=neo4j-enterprise-4.4.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 03 Aug 2023 21:40:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
# Thu, 03 Aug 2023 21:40:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 03 Aug 2023 21:40:48 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Thu, 03 Aug 2023 21:41:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.24-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 21:41:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 21:41:07 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Aug 2023 21:41:08 GMT
VOLUME [/data /logs]
# Thu, 03 Aug 2023 21:41:08 GMT
EXPOSE 7473 7474 7687
# Thu, 03 Aug 2023 21:41:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:41:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f2de644281932f812dc6760827991ae5ed5aba2a3bc3c4f617f109f75f6b20`  
		Last Modified: Fri, 28 Jul 2023 14:29:12 GMT  
		Size: 141.6 MB (141565323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7250bd21ad398820f23a94dcd2eba7e4f43ca58d419ff96ea286c9e039af6dc9`  
		Last Modified: Thu, 03 Aug 2023 21:42:03 GMT  
		Size: 3.9 KB (3896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832b529f2810befbd8c1bb109b32c7457705482ec1efbbf636150ca7b3497b38`  
		Last Modified: Thu, 03 Aug 2023 21:42:03 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e6f3839812e504e4f913404e830558119e6f170196c32efbf37ff497cc9134`  
		Last Modified: Thu, 03 Aug 2023 21:42:18 GMT  
		Size: 221.6 MB (221643816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

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

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

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

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

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

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

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

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:b512b5d560dd2dde74ab24de87a78cdfff8d221b2f2999140b19f8eb4eca77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:09aea145846f07201f3aeeb7bbe63d2a66436015230331d88e5a8088158e09a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304288681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f5f832540ed2d5d700445bb595f5395431874378545f16bd2ba57815a0736`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:31 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:31 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e98f12f6078ede0953b297c237b7fc66a4fcc524b0f5a248999eb322500373`  
		Last Modified: Wed, 26 Jul 2023 00:24:40 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef88f0476e9bc3f28cd01a098605d893b9e20323c4cffe39de539dd938ec9e0`  
		Last Modified: Wed, 26 Jul 2023 00:24:45 GMT  
		Size: 113.7 MB (113680638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d35b69a2650efbda5165fbba48ea3eac0c0e42aa090547480b1aadd590894826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301259723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8ab932d6ca7ae57a4980c4cbfc8ad6e7bfc930db5ba1552866ad5b6aa30d5`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:15 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:19 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:19 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104434b7ccf581e2d0346ee89bb50d552d6d09fa9973a74243845a2cfec8a9`  
		Last Modified: Tue, 25 Jul 2023 23:20:16 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aedca6d51bfb3ccf3ba7a027a966b0ca25f6b18fa70b9fb2e41044e686b9e`  
		Last Modified: Tue, 25 Jul 2023 23:20:21 GMT  
		Size: 113.7 MB (113680594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:cef81d3b779ac3266ea04403a00e63b3e11ec929119a6c88f45b0a3d5d70ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2c25d2d2659c52b84e310dae84356bd07f4244ff2bc4a4314fbef2f7d0880e60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574730721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d4a95cb4fd0445043173989c7f57b4579546a2f935a385b5fa4ae63b5b6a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:46 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:46 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0227d662ab242c2d0ffa72755321401e928b906d2eecc18bc421d1f296c75cee`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf896a3a9e0d2f5d023d959bf55709059d234e7273af4de941df0172767de2bc`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5402e14c7ece79c18fbd071b01ecf0116ea23a867b41eb99febd49fb8c2668d`  
		Last Modified: Fri, 28 Jul 2023 02:25:11 GMT  
		Size: 398.5 MB (398526166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8049fe405a4abada7285fec6234a785509e56ea3406ee800f8fc71cc9c422dc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.0 MB (572032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e259fae51df075ac8771ed97a2189e8084ec96359d21ea0bbdb7bc1312809af`
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
# Fri, 28 Jul 2023 14:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 14:25:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 14:26:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:26:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:26:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 14:26:17 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 14:26:17 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 14:26:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:26:17 GMT
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
	-	`sha256:3897d4be236e599dbb84cf9e606295b32f9d6eb93f96c886aca6b23aab621e5e`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352c325490be4fe2655a7ff92b9b17449f60176c2b59a9fce4e7dbb2c683f71c`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffacc759ff85182ca8c8f2342348bc52d714819bd3c1415096594bbd6d928e2`  
		Last Modified: Fri, 28 Jul 2023 14:28:36 GMT  
		Size: 398.4 MB (398417923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:cef81d3b779ac3266ea04403a00e63b3e11ec929119a6c88f45b0a3d5d70ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2c25d2d2659c52b84e310dae84356bd07f4244ff2bc4a4314fbef2f7d0880e60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574730721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d4a95cb4fd0445043173989c7f57b4579546a2f935a385b5fa4ae63b5b6a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:46 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:46 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0227d662ab242c2d0ffa72755321401e928b906d2eecc18bc421d1f296c75cee`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf896a3a9e0d2f5d023d959bf55709059d234e7273af4de941df0172767de2bc`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5402e14c7ece79c18fbd071b01ecf0116ea23a867b41eb99febd49fb8c2668d`  
		Last Modified: Fri, 28 Jul 2023 02:25:11 GMT  
		Size: 398.5 MB (398526166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8049fe405a4abada7285fec6234a785509e56ea3406ee800f8fc71cc9c422dc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.0 MB (572032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e259fae51df075ac8771ed97a2189e8084ec96359d21ea0bbdb7bc1312809af`
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
# Fri, 28 Jul 2023 14:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 14:25:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 14:26:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:26:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:26:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 14:26:17 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 14:26:17 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 14:26:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:26:17 GMT
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
	-	`sha256:3897d4be236e599dbb84cf9e606295b32f9d6eb93f96c886aca6b23aab621e5e`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352c325490be4fe2655a7ff92b9b17449f60176c2b59a9fce4e7dbb2c683f71c`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffacc759ff85182ca8c8f2342348bc52d714819bd3c1415096594bbd6d928e2`  
		Last Modified: Fri, 28 Jul 2023 14:28:36 GMT  
		Size: 398.4 MB (398417923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:6e3bfcc9c5c1601b141d82632c7c7143310c6d77a71da052fa31e075de663769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1c35f48031ff9f263daf74e96519af7f00ed9474c5d119c2443d8c82628f4c71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585324062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6830cfe48ed5ed4554ec8180269282d3a438ff419bfe2aa0406edfbe195749ef`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:49 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:49 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:49 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782497ca4d56a2b7cef6a438670bb57314b52ee19243cb1349f2249b6ed9e624`  
		Last Modified: Wed, 26 Jul 2023 00:25:11 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc46c09615ae6c70d16c9c43c9d8792195f0073ebde2bde194b686819394be6`  
		Last Modified: Wed, 26 Jul 2023 00:25:26 GMT  
		Size: 394.7 MB (394716020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d0cdaaa423f1f845ba0d19970a5119b32c5a8ff86302e76ae726e160d400dde2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582295089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409ffef3d14dcc0fda67824c2ea5cc2cb66b80c4a47c48128ba861649f751010`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:23 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:36 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:36 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:36 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1182b733d31f9d2f2480d4b6b1da1fa780d6044b8d87a348615c90fe26a02c91`  
		Last Modified: Tue, 25 Jul 2023 23:20:45 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e04c4fd165185817191dc8af19dcfc03a990879bafd31f95192de9040e8ab9d`  
		Last Modified: Tue, 25 Jul 2023 23:20:59 GMT  
		Size: 394.7 MB (394715960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:b512b5d560dd2dde74ab24de87a78cdfff8d221b2f2999140b19f8eb4eca77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:09aea145846f07201f3aeeb7bbe63d2a66436015230331d88e5a8088158e09a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304288681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f5f832540ed2d5d700445bb595f5395431874378545f16bd2ba57815a0736`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:31 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:31 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e98f12f6078ede0953b297c237b7fc66a4fcc524b0f5a248999eb322500373`  
		Last Modified: Wed, 26 Jul 2023 00:24:40 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef88f0476e9bc3f28cd01a098605d893b9e20323c4cffe39de539dd938ec9e0`  
		Last Modified: Wed, 26 Jul 2023 00:24:45 GMT  
		Size: 113.7 MB (113680638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d35b69a2650efbda5165fbba48ea3eac0c0e42aa090547480b1aadd590894826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301259723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8ab932d6ca7ae57a4980c4cbfc8ad6e7bfc930db5ba1552866ad5b6aa30d5`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:15 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:19 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:19 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104434b7ccf581e2d0346ee89bb50d552d6d09fa9973a74243845a2cfec8a9`  
		Last Modified: Tue, 25 Jul 2023 23:20:16 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aedca6d51bfb3ccf3ba7a027a966b0ca25f6b18fa70b9fb2e41044e686b9e`  
		Last Modified: Tue, 25 Jul 2023 23:20:21 GMT  
		Size: 113.7 MB (113680594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10` - linux; arm64 variant v8

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

## `neo4j:5.10-bullseye`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10-bullseye` - linux; arm64 variant v8

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

## `neo4j:5.10-community`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10-community` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10-community` - linux; arm64 variant v8

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

## `neo4j:5.10-community-bullseye`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10-community-bullseye` - linux; arm64 variant v8

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

## `neo4j:5.10-community-ubi8`

```console
$ docker pull neo4j@sha256:b512b5d560dd2dde74ab24de87a78cdfff8d221b2f2999140b19f8eb4eca77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:09aea145846f07201f3aeeb7bbe63d2a66436015230331d88e5a8088158e09a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304288681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f5f832540ed2d5d700445bb595f5395431874378545f16bd2ba57815a0736`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:31 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:31 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e98f12f6078ede0953b297c237b7fc66a4fcc524b0f5a248999eb322500373`  
		Last Modified: Wed, 26 Jul 2023 00:24:40 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef88f0476e9bc3f28cd01a098605d893b9e20323c4cffe39de539dd938ec9e0`  
		Last Modified: Wed, 26 Jul 2023 00:24:45 GMT  
		Size: 113.7 MB (113680638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d35b69a2650efbda5165fbba48ea3eac0c0e42aa090547480b1aadd590894826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301259723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8ab932d6ca7ae57a4980c4cbfc8ad6e7bfc930db5ba1552866ad5b6aa30d5`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:15 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:19 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:19 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104434b7ccf581e2d0346ee89bb50d552d6d09fa9973a74243845a2cfec8a9`  
		Last Modified: Tue, 25 Jul 2023 23:20:16 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aedca6d51bfb3ccf3ba7a027a966b0ca25f6b18fa70b9fb2e41044e686b9e`  
		Last Modified: Tue, 25 Jul 2023 23:20:21 GMT  
		Size: 113.7 MB (113680594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10-enterprise`

```console
$ docker pull neo4j@sha256:cef81d3b779ac3266ea04403a00e63b3e11ec929119a6c88f45b0a3d5d70ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2c25d2d2659c52b84e310dae84356bd07f4244ff2bc4a4314fbef2f7d0880e60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574730721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d4a95cb4fd0445043173989c7f57b4579546a2f935a385b5fa4ae63b5b6a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:46 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:46 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0227d662ab242c2d0ffa72755321401e928b906d2eecc18bc421d1f296c75cee`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf896a3a9e0d2f5d023d959bf55709059d234e7273af4de941df0172767de2bc`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5402e14c7ece79c18fbd071b01ecf0116ea23a867b41eb99febd49fb8c2668d`  
		Last Modified: Fri, 28 Jul 2023 02:25:11 GMT  
		Size: 398.5 MB (398526166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8049fe405a4abada7285fec6234a785509e56ea3406ee800f8fc71cc9c422dc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.0 MB (572032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e259fae51df075ac8771ed97a2189e8084ec96359d21ea0bbdb7bc1312809af`
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
# Fri, 28 Jul 2023 14:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 14:25:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 14:26:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:26:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:26:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 14:26:17 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 14:26:17 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 14:26:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:26:17 GMT
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
	-	`sha256:3897d4be236e599dbb84cf9e606295b32f9d6eb93f96c886aca6b23aab621e5e`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352c325490be4fe2655a7ff92b9b17449f60176c2b59a9fce4e7dbb2c683f71c`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffacc759ff85182ca8c8f2342348bc52d714819bd3c1415096594bbd6d928e2`  
		Last Modified: Fri, 28 Jul 2023 14:28:36 GMT  
		Size: 398.4 MB (398417923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:cef81d3b779ac3266ea04403a00e63b3e11ec929119a6c88f45b0a3d5d70ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2c25d2d2659c52b84e310dae84356bd07f4244ff2bc4a4314fbef2f7d0880e60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574730721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d4a95cb4fd0445043173989c7f57b4579546a2f935a385b5fa4ae63b5b6a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:46 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:46 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0227d662ab242c2d0ffa72755321401e928b906d2eecc18bc421d1f296c75cee`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf896a3a9e0d2f5d023d959bf55709059d234e7273af4de941df0172767de2bc`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5402e14c7ece79c18fbd071b01ecf0116ea23a867b41eb99febd49fb8c2668d`  
		Last Modified: Fri, 28 Jul 2023 02:25:11 GMT  
		Size: 398.5 MB (398526166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8049fe405a4abada7285fec6234a785509e56ea3406ee800f8fc71cc9c422dc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.0 MB (572032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e259fae51df075ac8771ed97a2189e8084ec96359d21ea0bbdb7bc1312809af`
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
# Fri, 28 Jul 2023 14:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 14:25:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 14:26:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:26:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:26:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 14:26:17 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 14:26:17 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 14:26:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:26:17 GMT
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
	-	`sha256:3897d4be236e599dbb84cf9e606295b32f9d6eb93f96c886aca6b23aab621e5e`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352c325490be4fe2655a7ff92b9b17449f60176c2b59a9fce4e7dbb2c683f71c`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffacc759ff85182ca8c8f2342348bc52d714819bd3c1415096594bbd6d928e2`  
		Last Modified: Fri, 28 Jul 2023 14:28:36 GMT  
		Size: 398.4 MB (398417923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:6e3bfcc9c5c1601b141d82632c7c7143310c6d77a71da052fa31e075de663769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1c35f48031ff9f263daf74e96519af7f00ed9474c5d119c2443d8c82628f4c71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585324062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6830cfe48ed5ed4554ec8180269282d3a438ff419bfe2aa0406edfbe195749ef`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:49 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:49 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:49 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782497ca4d56a2b7cef6a438670bb57314b52ee19243cb1349f2249b6ed9e624`  
		Last Modified: Wed, 26 Jul 2023 00:25:11 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc46c09615ae6c70d16c9c43c9d8792195f0073ebde2bde194b686819394be6`  
		Last Modified: Wed, 26 Jul 2023 00:25:26 GMT  
		Size: 394.7 MB (394716020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d0cdaaa423f1f845ba0d19970a5119b32c5a8ff86302e76ae726e160d400dde2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582295089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409ffef3d14dcc0fda67824c2ea5cc2cb66b80c4a47c48128ba861649f751010`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:23 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:36 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:36 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:36 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1182b733d31f9d2f2480d4b6b1da1fa780d6044b8d87a348615c90fe26a02c91`  
		Last Modified: Tue, 25 Jul 2023 23:20:45 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e04c4fd165185817191dc8af19dcfc03a990879bafd31f95192de9040e8ab9d`  
		Last Modified: Tue, 25 Jul 2023 23:20:59 GMT  
		Size: 394.7 MB (394715960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10-ubi8`

```console
$ docker pull neo4j@sha256:b512b5d560dd2dde74ab24de87a78cdfff8d221b2f2999140b19f8eb4eca77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:09aea145846f07201f3aeeb7bbe63d2a66436015230331d88e5a8088158e09a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304288681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f5f832540ed2d5d700445bb595f5395431874378545f16bd2ba57815a0736`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:31 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:31 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e98f12f6078ede0953b297c237b7fc66a4fcc524b0f5a248999eb322500373`  
		Last Modified: Wed, 26 Jul 2023 00:24:40 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef88f0476e9bc3f28cd01a098605d893b9e20323c4cffe39de539dd938ec9e0`  
		Last Modified: Wed, 26 Jul 2023 00:24:45 GMT  
		Size: 113.7 MB (113680638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d35b69a2650efbda5165fbba48ea3eac0c0e42aa090547480b1aadd590894826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301259723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8ab932d6ca7ae57a4980c4cbfc8ad6e7bfc930db5ba1552866ad5b6aa30d5`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:15 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:19 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:19 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104434b7ccf581e2d0346ee89bb50d552d6d09fa9973a74243845a2cfec8a9`  
		Last Modified: Tue, 25 Jul 2023 23:20:16 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aedca6d51bfb3ccf3ba7a027a966b0ca25f6b18fa70b9fb2e41044e686b9e`  
		Last Modified: Tue, 25 Jul 2023 23:20:21 GMT  
		Size: 113.7 MB (113680594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10.0`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10.0` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10.0` - linux; arm64 variant v8

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

## `neo4j:5.10.0-bullseye`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10.0-bullseye` - linux; arm64 variant v8

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

## `neo4j:5.10.0-community`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10.0-community` - linux; arm64 variant v8

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

## `neo4j:5.10.0-community-bullseye`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10.0-community-bullseye` - linux; arm64 variant v8

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

## `neo4j:5.10.0-community-ubi8`

```console
$ docker pull neo4j@sha256:b512b5d560dd2dde74ab24de87a78cdfff8d221b2f2999140b19f8eb4eca77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:09aea145846f07201f3aeeb7bbe63d2a66436015230331d88e5a8088158e09a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304288681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f5f832540ed2d5d700445bb595f5395431874378545f16bd2ba57815a0736`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:31 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:31 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e98f12f6078ede0953b297c237b7fc66a4fcc524b0f5a248999eb322500373`  
		Last Modified: Wed, 26 Jul 2023 00:24:40 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef88f0476e9bc3f28cd01a098605d893b9e20323c4cffe39de539dd938ec9e0`  
		Last Modified: Wed, 26 Jul 2023 00:24:45 GMT  
		Size: 113.7 MB (113680638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d35b69a2650efbda5165fbba48ea3eac0c0e42aa090547480b1aadd590894826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301259723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8ab932d6ca7ae57a4980c4cbfc8ad6e7bfc930db5ba1552866ad5b6aa30d5`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:15 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:19 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:19 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104434b7ccf581e2d0346ee89bb50d552d6d09fa9973a74243845a2cfec8a9`  
		Last Modified: Tue, 25 Jul 2023 23:20:16 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aedca6d51bfb3ccf3ba7a027a966b0ca25f6b18fa70b9fb2e41044e686b9e`  
		Last Modified: Tue, 25 Jul 2023 23:20:21 GMT  
		Size: 113.7 MB (113680594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10.0-enterprise`

```console
$ docker pull neo4j@sha256:cef81d3b779ac3266ea04403a00e63b3e11ec929119a6c88f45b0a3d5d70ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2c25d2d2659c52b84e310dae84356bd07f4244ff2bc4a4314fbef2f7d0880e60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574730721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d4a95cb4fd0445043173989c7f57b4579546a2f935a385b5fa4ae63b5b6a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:46 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:46 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0227d662ab242c2d0ffa72755321401e928b906d2eecc18bc421d1f296c75cee`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf896a3a9e0d2f5d023d959bf55709059d234e7273af4de941df0172767de2bc`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5402e14c7ece79c18fbd071b01ecf0116ea23a867b41eb99febd49fb8c2668d`  
		Last Modified: Fri, 28 Jul 2023 02:25:11 GMT  
		Size: 398.5 MB (398526166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8049fe405a4abada7285fec6234a785509e56ea3406ee800f8fc71cc9c422dc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.0 MB (572032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e259fae51df075ac8771ed97a2189e8084ec96359d21ea0bbdb7bc1312809af`
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
# Fri, 28 Jul 2023 14:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 14:25:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 14:26:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:26:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:26:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 14:26:17 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 14:26:17 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 14:26:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:26:17 GMT
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
	-	`sha256:3897d4be236e599dbb84cf9e606295b32f9d6eb93f96c886aca6b23aab621e5e`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352c325490be4fe2655a7ff92b9b17449f60176c2b59a9fce4e7dbb2c683f71c`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffacc759ff85182ca8c8f2342348bc52d714819bd3c1415096594bbd6d928e2`  
		Last Modified: Fri, 28 Jul 2023 14:28:36 GMT  
		Size: 398.4 MB (398417923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:cef81d3b779ac3266ea04403a00e63b3e11ec929119a6c88f45b0a3d5d70ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2c25d2d2659c52b84e310dae84356bd07f4244ff2bc4a4314fbef2f7d0880e60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574730721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d4a95cb4fd0445043173989c7f57b4579546a2f935a385b5fa4ae63b5b6a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:46 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:46 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0227d662ab242c2d0ffa72755321401e928b906d2eecc18bc421d1f296c75cee`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf896a3a9e0d2f5d023d959bf55709059d234e7273af4de941df0172767de2bc`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5402e14c7ece79c18fbd071b01ecf0116ea23a867b41eb99febd49fb8c2668d`  
		Last Modified: Fri, 28 Jul 2023 02:25:11 GMT  
		Size: 398.5 MB (398526166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8049fe405a4abada7285fec6234a785509e56ea3406ee800f8fc71cc9c422dc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.0 MB (572032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e259fae51df075ac8771ed97a2189e8084ec96359d21ea0bbdb7bc1312809af`
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
# Fri, 28 Jul 2023 14:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 14:25:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 14:26:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:26:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:26:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 14:26:17 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 14:26:17 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 14:26:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:26:17 GMT
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
	-	`sha256:3897d4be236e599dbb84cf9e606295b32f9d6eb93f96c886aca6b23aab621e5e`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352c325490be4fe2655a7ff92b9b17449f60176c2b59a9fce4e7dbb2c683f71c`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffacc759ff85182ca8c8f2342348bc52d714819bd3c1415096594bbd6d928e2`  
		Last Modified: Fri, 28 Jul 2023 14:28:36 GMT  
		Size: 398.4 MB (398417923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:6e3bfcc9c5c1601b141d82632c7c7143310c6d77a71da052fa31e075de663769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1c35f48031ff9f263daf74e96519af7f00ed9474c5d119c2443d8c82628f4c71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585324062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6830cfe48ed5ed4554ec8180269282d3a438ff419bfe2aa0406edfbe195749ef`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:49 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:49 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:49 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782497ca4d56a2b7cef6a438670bb57314b52ee19243cb1349f2249b6ed9e624`  
		Last Modified: Wed, 26 Jul 2023 00:25:11 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc46c09615ae6c70d16c9c43c9d8792195f0073ebde2bde194b686819394be6`  
		Last Modified: Wed, 26 Jul 2023 00:25:26 GMT  
		Size: 394.7 MB (394716020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d0cdaaa423f1f845ba0d19970a5119b32c5a8ff86302e76ae726e160d400dde2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582295089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409ffef3d14dcc0fda67824c2ea5cc2cb66b80c4a47c48128ba861649f751010`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:23 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:36 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:36 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:36 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1182b733d31f9d2f2480d4b6b1da1fa780d6044b8d87a348615c90fe26a02c91`  
		Last Modified: Tue, 25 Jul 2023 23:20:45 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e04c4fd165185817191dc8af19dcfc03a990879bafd31f95192de9040e8ab9d`  
		Last Modified: Tue, 25 Jul 2023 23:20:59 GMT  
		Size: 394.7 MB (394715960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.10.0-ubi8`

```console
$ docker pull neo4j@sha256:b512b5d560dd2dde74ab24de87a78cdfff8d221b2f2999140b19f8eb4eca77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.10.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:09aea145846f07201f3aeeb7bbe63d2a66436015230331d88e5a8088158e09a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304288681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f5f832540ed2d5d700445bb595f5395431874378545f16bd2ba57815a0736`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:31 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:31 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e98f12f6078ede0953b297c237b7fc66a4fcc524b0f5a248999eb322500373`  
		Last Modified: Wed, 26 Jul 2023 00:24:40 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef88f0476e9bc3f28cd01a098605d893b9e20323c4cffe39de539dd938ec9e0`  
		Last Modified: Wed, 26 Jul 2023 00:24:45 GMT  
		Size: 113.7 MB (113680638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.10.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d35b69a2650efbda5165fbba48ea3eac0c0e42aa090547480b1aadd590894826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301259723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8ab932d6ca7ae57a4980c4cbfc8ad6e7bfc930db5ba1552866ad5b6aa30d5`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:15 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:19 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:19 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104434b7ccf581e2d0346ee89bb50d552d6d09fa9973a74243845a2cfec8a9`  
		Last Modified: Tue, 25 Jul 2023 23:20:16 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aedca6d51bfb3ccf3ba7a027a966b0ca25f6b18fa70b9fb2e41044e686b9e`  
		Last Modified: Tue, 25 Jul 2023 23:20:21 GMT  
		Size: 113.7 MB (113680594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
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

## `neo4j:community`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

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

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

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

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:b512b5d560dd2dde74ab24de87a78cdfff8d221b2f2999140b19f8eb4eca77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:09aea145846f07201f3aeeb7bbe63d2a66436015230331d88e5a8088158e09a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304288681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f5f832540ed2d5d700445bb595f5395431874378545f16bd2ba57815a0736`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:31 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:31 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e98f12f6078ede0953b297c237b7fc66a4fcc524b0f5a248999eb322500373`  
		Last Modified: Wed, 26 Jul 2023 00:24:40 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef88f0476e9bc3f28cd01a098605d893b9e20323c4cffe39de539dd938ec9e0`  
		Last Modified: Wed, 26 Jul 2023 00:24:45 GMT  
		Size: 113.7 MB (113680638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d35b69a2650efbda5165fbba48ea3eac0c0e42aa090547480b1aadd590894826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301259723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8ab932d6ca7ae57a4980c4cbfc8ad6e7bfc930db5ba1552866ad5b6aa30d5`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:15 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:19 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:19 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104434b7ccf581e2d0346ee89bb50d552d6d09fa9973a74243845a2cfec8a9`  
		Last Modified: Tue, 25 Jul 2023 23:20:16 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aedca6d51bfb3ccf3ba7a027a966b0ca25f6b18fa70b9fb2e41044e686b9e`  
		Last Modified: Tue, 25 Jul 2023 23:20:21 GMT  
		Size: 113.7 MB (113680594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:cef81d3b779ac3266ea04403a00e63b3e11ec929119a6c88f45b0a3d5d70ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2c25d2d2659c52b84e310dae84356bd07f4244ff2bc4a4314fbef2f7d0880e60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574730721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d4a95cb4fd0445043173989c7f57b4579546a2f935a385b5fa4ae63b5b6a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:46 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:46 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0227d662ab242c2d0ffa72755321401e928b906d2eecc18bc421d1f296c75cee`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf896a3a9e0d2f5d023d959bf55709059d234e7273af4de941df0172767de2bc`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5402e14c7ece79c18fbd071b01ecf0116ea23a867b41eb99febd49fb8c2668d`  
		Last Modified: Fri, 28 Jul 2023 02:25:11 GMT  
		Size: 398.5 MB (398526166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8049fe405a4abada7285fec6234a785509e56ea3406ee800f8fc71cc9c422dc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.0 MB (572032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e259fae51df075ac8771ed97a2189e8084ec96359d21ea0bbdb7bc1312809af`
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
# Fri, 28 Jul 2023 14:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 14:25:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 14:26:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:26:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:26:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 14:26:17 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 14:26:17 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 14:26:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:26:17 GMT
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
	-	`sha256:3897d4be236e599dbb84cf9e606295b32f9d6eb93f96c886aca6b23aab621e5e`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352c325490be4fe2655a7ff92b9b17449f60176c2b59a9fce4e7dbb2c683f71c`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffacc759ff85182ca8c8f2342348bc52d714819bd3c1415096594bbd6d928e2`  
		Last Modified: Fri, 28 Jul 2023 14:28:36 GMT  
		Size: 398.4 MB (398417923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:cef81d3b779ac3266ea04403a00e63b3e11ec929119a6c88f45b0a3d5d70ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2c25d2d2659c52b84e310dae84356bd07f4244ff2bc4a4314fbef2f7d0880e60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574730721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d4a95cb4fd0445043173989c7f57b4579546a2f935a385b5fa4ae63b5b6a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:46 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:46 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0227d662ab242c2d0ffa72755321401e928b906d2eecc18bc421d1f296c75cee`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf896a3a9e0d2f5d023d959bf55709059d234e7273af4de941df0172767de2bc`  
		Last Modified: Fri, 28 Jul 2023 02:24:52 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5402e14c7ece79c18fbd071b01ecf0116ea23a867b41eb99febd49fb8c2668d`  
		Last Modified: Fri, 28 Jul 2023 02:25:11 GMT  
		Size: 398.5 MB (398526166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8049fe405a4abada7285fec6234a785509e56ea3406ee800f8fc71cc9c422dc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.0 MB (572032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e259fae51df075ac8771ed97a2189e8084ec96359d21ea0bbdb7bc1312809af`
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
# Fri, 28 Jul 2023 14:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 14:25:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 14:25:48 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 14:26:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:26:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:26:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 14:26:17 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 14:26:17 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 14:26:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 14:26:17 GMT
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
	-	`sha256:3897d4be236e599dbb84cf9e606295b32f9d6eb93f96c886aca6b23aab621e5e`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352c325490be4fe2655a7ff92b9b17449f60176c2b59a9fce4e7dbb2c683f71c`  
		Last Modified: Fri, 28 Jul 2023 14:28:14 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffacc759ff85182ca8c8f2342348bc52d714819bd3c1415096594bbd6d928e2`  
		Last Modified: Fri, 28 Jul 2023 14:28:36 GMT  
		Size: 398.4 MB (398417923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:6e3bfcc9c5c1601b141d82632c7c7143310c6d77a71da052fa31e075de663769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1c35f48031ff9f263daf74e96519af7f00ed9474c5d119c2443d8c82628f4c71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585324062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6830cfe48ed5ed4554ec8180269282d3a438ff419bfe2aa0406edfbe195749ef`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:37 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:49 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:49 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:49 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782497ca4d56a2b7cef6a438670bb57314b52ee19243cb1349f2249b6ed9e624`  
		Last Modified: Wed, 26 Jul 2023 00:25:11 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc46c09615ae6c70d16c9c43c9d8792195f0073ebde2bde194b686819394be6`  
		Last Modified: Wed, 26 Jul 2023 00:25:26 GMT  
		Size: 394.7 MB (394716020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d0cdaaa423f1f845ba0d19970a5119b32c5a8ff86302e76ae726e160d400dde2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582295089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409ffef3d14dcc0fda67824c2ea5cc2cb66b80c4a47c48128ba861649f751010`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:23 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:36 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:36 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:36 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1182b733d31f9d2f2480d4b6b1da1fa780d6044b8d87a348615c90fe26a02c91`  
		Last Modified: Tue, 25 Jul 2023 23:20:45 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e04c4fd165185817191dc8af19dcfc03a990879bafd31f95192de9040e8ab9d`  
		Last Modified: Tue, 25 Jul 2023 23:20:59 GMT  
		Size: 394.7 MB (394715960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:50fa92f6e46746c33892bd9fb110f7e085e6e7a501ebf82481e352b24e4f7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:13d0cdc950c0b934a2011b75a0270a16fb7b996bfcdd08728151d9470759c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293694688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d2d9f1777ecaa8cb5431e8b52075c18c6ee52e4452b5559cf3ada99dbf5d6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 28 Jul 2023 02:22:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Fri, 28 Jul 2023 02:22:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 28 Jul 2023 02:22:10 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Fri, 28 Jul 2023 02:22:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:22:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 02:22:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 28 Jul 2023 02:22:22 GMT
VOLUME [/data /logs]
# Fri, 28 Jul 2023 02:22:22 GMT
EXPOSE 7473 7474 7687
# Fri, 28 Jul 2023 02:22:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:22:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49c7a8e28a578f2106efec5e3ac93573fa9f79749b6c0caf76db9dd3f4fec7a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f3336e435a053cef56b0f8c20cf85bf85cead29294b06742dbd2c7e417f8a`  
		Last Modified: Fri, 28 Jul 2023 02:24:07 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574be4fcc33dd7feb229816b06b03cd8ac05032b7c6837fae5b3fb7cce1ca8f3`  
		Last Modified: Fri, 28 Jul 2023 02:24:14 GMT  
		Size: 117.5 MB (117490129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

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

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:b512b5d560dd2dde74ab24de87a78cdfff8d221b2f2999140b19f8eb4eca77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:09aea145846f07201f3aeeb7bbe63d2a66436015230331d88e5a8088158e09a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304288681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f5f832540ed2d5d700445bb595f5395431874378545f16bd2ba57815a0736`
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
# Wed, 26 Jul 2023 00:22:18 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Wed, 26 Jul 2023 00:22:26 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Wed, 26 Jul 2023 00:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Jul 2023 00:22:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Wed, 26 Jul 2023 00:22:27 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 26 Jul 2023 00:22:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Wed, 26 Jul 2023 00:22:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:22:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Jul 2023 00:22:31 GMT
VOLUME [/data /logs]
# Wed, 26 Jul 2023 00:22:31 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Jul 2023 00:22:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 00:22:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2b5f358ecf170222d561c3811b4d74699c0078ec14ffaa84434d303b0b3591f`  
		Last Modified: Tue, 16 May 2023 13:59:36 GMT  
		Size: 39.3 MB (39289044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56580895f273250b2f893a91ae9e8033e20eff4ba7fec53f9b0e6c12fa806708`  
		Last Modified: Wed, 26 Jul 2023 00:24:51 GMT  
		Size: 144.8 MB (144773713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83c349e24cb7a2c0851367eed074c901c22dceecef1c5b6224cab28d5729df`  
		Last Modified: Wed, 26 Jul 2023 00:24:41 GMT  
		Size: 6.5 MB (6535936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e98f12f6078ede0953b297c237b7fc66a4fcc524b0f5a248999eb322500373`  
		Last Modified: Wed, 26 Jul 2023 00:24:40 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef88f0476e9bc3f28cd01a098605d893b9e20323c4cffe39de539dd938ec9e0`  
		Last Modified: Wed, 26 Jul 2023 00:24:45 GMT  
		Size: 113.7 MB (113680638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d35b69a2650efbda5165fbba48ea3eac0c0e42aa090547480b1aadd590894826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301259723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf8ab932d6ca7ae57a4980c4cbfc8ad6e7bfc930db5ba1552866ad5b6aa30d5`
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
# Tue, 25 Jul 2023 23:18:04 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:18:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 25 Jul 2023 23:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 25 Jul 2023 23:18:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Tue, 25 Jul 2023 23:18:15 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Tue, 25 Jul 2023 23:18:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 25 Jul 2023 23:18:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:18:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 25 Jul 2023 23:18:19 GMT
VOLUME [/data /logs]
# Tue, 25 Jul 2023 23:18:19 GMT
EXPOSE 7473 7474 7687
# Tue, 25 Jul 2023 23:18:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 25 Jul 2023 23:18:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b964235f9f3052ef964da88e3540367964bd517e4c985fcdc8a6b705c48326ed`  
		Last Modified: Tue, 16 May 2023 16:09:53 GMT  
		Size: 37.5 MB (37531440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b77d66a4dcb171787aac89d9bc6389403738a0c44316f38daa338e3b7aa2e`  
		Last Modified: Tue, 25 Jul 2023 23:20:25 GMT  
		Size: 143.5 MB (143538036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ff368b4c00cb3ff4b2e2849bb2dc3d0de6a4f79dc61ad7b546cdc6d016f4c4`  
		Last Modified: Tue, 25 Jul 2023 23:20:17 GMT  
		Size: 6.5 MB (6500303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104434b7ccf581e2d0346ee89bb50d552d6d09fa9973a74243845a2cfec8a9`  
		Last Modified: Tue, 25 Jul 2023 23:20:16 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aedca6d51bfb3ccf3ba7a027a966b0ca25f6b18fa70b9fb2e41044e686b9e`  
		Last Modified: Tue, 25 Jul 2023 23:20:21 GMT  
		Size: 113.7 MB (113680594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
