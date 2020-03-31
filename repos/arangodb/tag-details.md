<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:2.8`](#arangodb28)
-	[`arangodb:2.8.11`](#arangodb2811)
-	[`arangodb:3.2`](#arangodb32)
-	[`arangodb:3.2.17`](#arangodb3217)
-	[`arangodb:3.3`](#arangodb33)
-	[`arangodb:3.3.25`](#arangodb3325)
-	[`arangodb:3.4`](#arangodb34)
-	[`arangodb:3.4.9`](#arangodb349)
-	[`arangodb:3.5`](#arangodb35)
-	[`arangodb:3.5.4`](#arangodb354)
-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.2`](#arangodb362)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:2.8`

```console
$ docker pull arangodb@sha256:c2e71091305c052fcddd392e6e5fdf02657c58d286261c8e6589c5cc33bb3bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:2.8` - linux; amd64

```console
$ docker pull arangodb@sha256:5c55a80cf44d38be3a0460b80da50effe300f172713e51979c429213f0f51e41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115105188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a1db9d92bcbbb4ebc7bb887da74fa53b667f464f31892f9867b4caa7765099`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:15 GMT
ADD file:00e3c0ca649cf82da02cd7fec7b3121205c2c54c4569209a2212c4924c73d5a9 in / 
# Tue, 31 Mar 2020 01:21:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:45:52 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 31 Mar 2020 01:45:53 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 31 Mar 2020 01:45:53 GMT
ENV ARCHITECTURE=amd64
# Tue, 31 Mar 2020 01:45:53 GMT
ENV ARANGO_VERSION=2.8.11
# Tue, 31 Mar 2020 01:45:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb2/Debian_8.0
# Tue, 31 Mar 2020 01:45:53 GMT
ENV ARANGO_PACKAGE=arangodb_2.8.11_amd64.deb
# Tue, 31 Mar 2020 01:45:54 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb
# Tue, 31 Mar 2020 01:45:54 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb.asc
# Tue, 31 Mar 2020 01:48:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libgoogle-perftools4         ca-certificates         pwgen         wget     &&     rm -rf /var/lib/apt/lists/* &&     wget ${ARANGO_SIGNATURE_URL} &&           wget ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     dpkg -i ${ARANGO_PACKAGE} &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb/arangod.conf     &&     apt-get purge -y --auto-remove ca-certificates wget &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 31 Mar 2020 01:48:09 GMT
RUN chown arangodb:arangodb /var/lib/arangodb &&   chown arangodb:arangodb /var/lib/arangodb-apps
# Tue, 31 Mar 2020 01:48:09 GMT
VOLUME [/var/lib/arangodb /var/lib/arangodb-apps]
# Tue, 31 Mar 2020 01:48:09 GMT
COPY file:9a5bd6b5ab4e3a7842ac5f3e59bb9907920e9e2dc31d297c3676110b569a9d7e in /entrypoint.sh 
# Tue, 31 Mar 2020 01:48:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 01:48:10 GMT
EXPOSE 8529
# Tue, 31 Mar 2020 01:48:10 GMT
USER arangodb
# Tue, 31 Mar 2020 01:48:10 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f27d6ed8cebc4be4a992767cb74cd433e5e145ae55c57e9e913e47d315b1dbdf`  
		Last Modified: Tue, 31 Mar 2020 01:26:56 GMT  
		Size: 54.4 MB (54389951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6321e0c5cf3273af656e6f08667c0ce79009535c6256f8d356831d43c2deac4`  
		Last Modified: Tue, 31 Mar 2020 01:50:19 GMT  
		Size: 8.6 KB (8594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5ca9535820105cdfbcdced27c1b8bb4f7c13ba09ed0bd9ee29ae320afba6a7`  
		Last Modified: Tue, 31 Mar 2020 01:50:29 GMT  
		Size: 60.7 MB (60705382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047ea38c32863d85eab5df6c13b66ef40d0e1253dcc268767409ae2d9239d508`  
		Last Modified: Tue, 31 Mar 2020 01:50:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac13c18eb9e829001d47cb3a35804afdd67c6d7eeb91d04b206640b5f6d2b9f3`  
		Last Modified: Tue, 31 Mar 2020 01:50:19 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:2.8.11`

```console
$ docker pull arangodb@sha256:c2e71091305c052fcddd392e6e5fdf02657c58d286261c8e6589c5cc33bb3bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:2.8.11` - linux; amd64

```console
$ docker pull arangodb@sha256:5c55a80cf44d38be3a0460b80da50effe300f172713e51979c429213f0f51e41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115105188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a1db9d92bcbbb4ebc7bb887da74fa53b667f464f31892f9867b4caa7765099`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:15 GMT
ADD file:00e3c0ca649cf82da02cd7fec7b3121205c2c54c4569209a2212c4924c73d5a9 in / 
# Tue, 31 Mar 2020 01:21:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:45:52 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 31 Mar 2020 01:45:53 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 31 Mar 2020 01:45:53 GMT
ENV ARCHITECTURE=amd64
# Tue, 31 Mar 2020 01:45:53 GMT
ENV ARANGO_VERSION=2.8.11
# Tue, 31 Mar 2020 01:45:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb2/Debian_8.0
# Tue, 31 Mar 2020 01:45:53 GMT
ENV ARANGO_PACKAGE=arangodb_2.8.11_amd64.deb
# Tue, 31 Mar 2020 01:45:54 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb
# Tue, 31 Mar 2020 01:45:54 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb.asc
# Tue, 31 Mar 2020 01:48:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libgoogle-perftools4         ca-certificates         pwgen         wget     &&     rm -rf /var/lib/apt/lists/* &&     wget ${ARANGO_SIGNATURE_URL} &&           wget ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     dpkg -i ${ARANGO_PACKAGE} &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb/arangod.conf     &&     apt-get purge -y --auto-remove ca-certificates wget &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 31 Mar 2020 01:48:09 GMT
RUN chown arangodb:arangodb /var/lib/arangodb &&   chown arangodb:arangodb /var/lib/arangodb-apps
# Tue, 31 Mar 2020 01:48:09 GMT
VOLUME [/var/lib/arangodb /var/lib/arangodb-apps]
# Tue, 31 Mar 2020 01:48:09 GMT
COPY file:9a5bd6b5ab4e3a7842ac5f3e59bb9907920e9e2dc31d297c3676110b569a9d7e in /entrypoint.sh 
# Tue, 31 Mar 2020 01:48:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 01:48:10 GMT
EXPOSE 8529
# Tue, 31 Mar 2020 01:48:10 GMT
USER arangodb
# Tue, 31 Mar 2020 01:48:10 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f27d6ed8cebc4be4a992767cb74cd433e5e145ae55c57e9e913e47d315b1dbdf`  
		Last Modified: Tue, 31 Mar 2020 01:26:56 GMT  
		Size: 54.4 MB (54389951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6321e0c5cf3273af656e6f08667c0ce79009535c6256f8d356831d43c2deac4`  
		Last Modified: Tue, 31 Mar 2020 01:50:19 GMT  
		Size: 8.6 KB (8594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5ca9535820105cdfbcdced27c1b8bb4f7c13ba09ed0bd9ee29ae320afba6a7`  
		Last Modified: Tue, 31 Mar 2020 01:50:29 GMT  
		Size: 60.7 MB (60705382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047ea38c32863d85eab5df6c13b66ef40d0e1253dcc268767409ae2d9239d508`  
		Last Modified: Tue, 31 Mar 2020 01:50:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac13c18eb9e829001d47cb3a35804afdd67c6d7eeb91d04b206640b5f6d2b9f3`  
		Last Modified: Tue, 31 Mar 2020 01:50:19 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.2`

```console
$ docker pull arangodb@sha256:2ed0484cc2f2b9332477a90b02c54610de4fb2ce099580b3a4fb5926f73646e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.2` - linux; amd64

```console
$ docker pull arangodb@sha256:333a991911c4188184249940fc12453e335a4eb20edf8229cdb174ca631fe810
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113546208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd14a4004ab33d54b4b5ddbb5f9742202ba2ac345355a87ea622b3451b508330`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:48:21 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 31 Mar 2020 01:48:21 GMT
ENV ARCHITECTURE=amd64
# Tue, 31 Mar 2020 01:48:22 GMT
ENV DEB_PACKAGE_VERSION=1
# Tue, 31 Mar 2020 01:48:22 GMT
ENV ARANGO_VERSION=3.2.17
# Tue, 31 Mar 2020 01:48:22 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb32/Debian_9.0
# Tue, 31 Mar 2020 01:48:22 GMT
ENV ARANGO_PACKAGE=arangodb3-3.2.17-1_amd64.deb
# Tue, 31 Mar 2020 01:48:23 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.17-1_amd64.deb
# Tue, 31 Mar 2020 01:48:23 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.17-1_amd64.deb.asc
# Tue, 31 Mar 2020 01:48:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gpg dirmngr     &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:48:38 GMT
RUN gpg --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 31 Mar 2020 01:48:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libjemalloc1         ca-certificates         pwgen         curl         numactl     &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:48:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 01:49:03 GMT
RUN curl --fail -O ${ARANGO_SIGNATURE_URL} &&           curl --fail -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf     && chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps     && chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps     &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 31 Mar 2020 01:49:03 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 31 Mar 2020 01:49:03 GMT
COPY file:01bdd453b032c9d383e66c7e6332049490bb7877724d3bb90d185f11336934d2 in /entrypoint.sh 
# Tue, 31 Mar 2020 01:49:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 01:49:04 GMT
EXPOSE 8529
# Tue, 31 Mar 2020 01:49:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f6aef0da98ee751b078a15021057ff268f2a3c4ab106fc338f70625df5b76`  
		Last Modified: Tue, 31 Mar 2020 01:50:37 GMT  
		Size: 6.6 MB (6566484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328c1d7ab7114343121e79db1b4c08c72b380848e0cd8d5349225372d58207ab`  
		Last Modified: Tue, 31 Mar 2020 01:50:35 GMT  
		Size: 4.4 KB (4445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e639bf0ef428f9ad7ed6e23ea0532f2d4a5c5a36bd7d09d5c4d0d97527fb9d43`  
		Last Modified: Tue, 31 Mar 2020 01:50:36 GMT  
		Size: 7.5 MB (7461602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54d1b748826281d6b73ccc2e7a00d15eb7b4c05ba5982b877d7b4f9bf80af60`  
		Last Modified: Tue, 31 Mar 2020 01:50:35 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e84d43c5ad8ebf77644c925d810c9d6e82f05850444bb6c039efb8dec5f257b`  
		Last Modified: Tue, 31 Mar 2020 01:50:45 GMT  
		Size: 54.1 MB (54135598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70be59da3e4d08f102da036b186364c785d40ee8730750a0fa724727d559486`  
		Last Modified: Tue, 31 Mar 2020 01:50:35 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.2.17`

```console
$ docker pull arangodb@sha256:2ed0484cc2f2b9332477a90b02c54610de4fb2ce099580b3a4fb5926f73646e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.2.17` - linux; amd64

```console
$ docker pull arangodb@sha256:333a991911c4188184249940fc12453e335a4eb20edf8229cdb174ca631fe810
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113546208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd14a4004ab33d54b4b5ddbb5f9742202ba2ac345355a87ea622b3451b508330`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:48:21 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 31 Mar 2020 01:48:21 GMT
ENV ARCHITECTURE=amd64
# Tue, 31 Mar 2020 01:48:22 GMT
ENV DEB_PACKAGE_VERSION=1
# Tue, 31 Mar 2020 01:48:22 GMT
ENV ARANGO_VERSION=3.2.17
# Tue, 31 Mar 2020 01:48:22 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb32/Debian_9.0
# Tue, 31 Mar 2020 01:48:22 GMT
ENV ARANGO_PACKAGE=arangodb3-3.2.17-1_amd64.deb
# Tue, 31 Mar 2020 01:48:23 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.17-1_amd64.deb
# Tue, 31 Mar 2020 01:48:23 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.17-1_amd64.deb.asc
# Tue, 31 Mar 2020 01:48:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gpg dirmngr     &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:48:38 GMT
RUN gpg --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 31 Mar 2020 01:48:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libjemalloc1         ca-certificates         pwgen         curl         numactl     &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:48:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 01:49:03 GMT
RUN curl --fail -O ${ARANGO_SIGNATURE_URL} &&           curl --fail -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf     && chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps     && chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps     &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 31 Mar 2020 01:49:03 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 31 Mar 2020 01:49:03 GMT
COPY file:01bdd453b032c9d383e66c7e6332049490bb7877724d3bb90d185f11336934d2 in /entrypoint.sh 
# Tue, 31 Mar 2020 01:49:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 01:49:04 GMT
EXPOSE 8529
# Tue, 31 Mar 2020 01:49:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f6aef0da98ee751b078a15021057ff268f2a3c4ab106fc338f70625df5b76`  
		Last Modified: Tue, 31 Mar 2020 01:50:37 GMT  
		Size: 6.6 MB (6566484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328c1d7ab7114343121e79db1b4c08c72b380848e0cd8d5349225372d58207ab`  
		Last Modified: Tue, 31 Mar 2020 01:50:35 GMT  
		Size: 4.4 KB (4445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e639bf0ef428f9ad7ed6e23ea0532f2d4a5c5a36bd7d09d5c4d0d97527fb9d43`  
		Last Modified: Tue, 31 Mar 2020 01:50:36 GMT  
		Size: 7.5 MB (7461602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54d1b748826281d6b73ccc2e7a00d15eb7b4c05ba5982b877d7b4f9bf80af60`  
		Last Modified: Tue, 31 Mar 2020 01:50:35 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e84d43c5ad8ebf77644c925d810c9d6e82f05850444bb6c039efb8dec5f257b`  
		Last Modified: Tue, 31 Mar 2020 01:50:45 GMT  
		Size: 54.1 MB (54135598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70be59da3e4d08f102da036b186364c785d40ee8730750a0fa724727d559486`  
		Last Modified: Tue, 31 Mar 2020 01:50:35 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.3`

```console
$ docker pull arangodb@sha256:76e1296b258593ce16fbbf7796d4c100e01057a1caea7720b7d3a0a13abdb6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.3` - linux; amd64

```console
$ docker pull arangodb@sha256:2d2150ee21e435120dacd23355faf74bdc8c2a44c82663d6610fafb9b177e96b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117195912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f229738c441cadf9f4a72cf8184893bbfc9452b864e512f2547bf8d84ac87a31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:48:21 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 31 Mar 2020 01:48:21 GMT
ENV ARCHITECTURE=amd64
# Tue, 31 Mar 2020 01:48:22 GMT
ENV DEB_PACKAGE_VERSION=1
# Tue, 31 Mar 2020 01:49:13 GMT
ENV ARANGO_VERSION=3.3.25
# Tue, 31 Mar 2020 01:49:13 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb33/Debian_9.0
# Tue, 31 Mar 2020 01:49:14 GMT
ENV ARANGO_PACKAGE=arangodb3-3.3.25-1_amd64.deb
# Tue, 31 Mar 2020 01:49:14 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb33/Debian_9.0/amd64/arangodb3-3.3.25-1_amd64.deb
# Tue, 31 Mar 2020 01:49:14 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb33/Debian_9.0/amd64/arangodb3-3.3.25-1_amd64.deb.asc
# Tue, 31 Mar 2020 01:49:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         dirmngr         gpg     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:49:28 GMT
RUN gpg --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 31 Mar 2020 01:49:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         curl         libjemalloc1         libtasn1-6         numactl         openssl         pwgen         sensible-utils     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:49:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 01:49:52 GMT
RUN curl --fail -O ${ARANGO_SIGNATURE_URL} &&           curl --fail -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf     && chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps     && chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps     &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 31 Mar 2020 01:49:53 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 31 Mar 2020 01:49:53 GMT
COPY file:01bdd453b032c9d383e66c7e6332049490bb7877724d3bb90d185f11336934d2 in /entrypoint.sh 
# Tue, 31 Mar 2020 01:49:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 01:49:53 GMT
EXPOSE 8529
# Tue, 31 Mar 2020 01:49:53 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cbfdf7be5d0a9cfc6d40d0563d715456b491845f98c74cab7bba3dd90db998`  
		Last Modified: Tue, 31 Mar 2020 01:50:52 GMT  
		Size: 6.6 MB (6566458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc110f2972991d39fab4ccd21c634317136a6d2ac764a6a26003891586473f18`  
		Last Modified: Tue, 31 Mar 2020 01:50:50 GMT  
		Size: 4.4 KB (4447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fba0aecf02ac557cc6a7b1f48320843554cab334bbf392b4bd17eeb5b1506fa`  
		Last Modified: Tue, 31 Mar 2020 01:50:52 GMT  
		Size: 7.5 MB (7461612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28339a396e65dd149e1cc7e0bdb7c2a05c69ef850a95689f6fe7ed02bf36a2d0`  
		Last Modified: Tue, 31 Mar 2020 01:50:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e62b4fd0d0980ad90d579c2247248542a7f87f18b3c9eaf64cf5b1c2a0c4bf5`  
		Last Modified: Tue, 31 Mar 2020 01:51:02 GMT  
		Size: 57.8 MB (57785314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b50b1475da0f9343fabc7ab0309cfe831d1366a1a14560bcb47880f5f57c5c7`  
		Last Modified: Tue, 31 Mar 2020 01:50:50 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.3.25`

```console
$ docker pull arangodb@sha256:76e1296b258593ce16fbbf7796d4c100e01057a1caea7720b7d3a0a13abdb6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.3.25` - linux; amd64

```console
$ docker pull arangodb@sha256:2d2150ee21e435120dacd23355faf74bdc8c2a44c82663d6610fafb9b177e96b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117195912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f229738c441cadf9f4a72cf8184893bbfc9452b864e512f2547bf8d84ac87a31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:48:21 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 31 Mar 2020 01:48:21 GMT
ENV ARCHITECTURE=amd64
# Tue, 31 Mar 2020 01:48:22 GMT
ENV DEB_PACKAGE_VERSION=1
# Tue, 31 Mar 2020 01:49:13 GMT
ENV ARANGO_VERSION=3.3.25
# Tue, 31 Mar 2020 01:49:13 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb33/Debian_9.0
# Tue, 31 Mar 2020 01:49:14 GMT
ENV ARANGO_PACKAGE=arangodb3-3.3.25-1_amd64.deb
# Tue, 31 Mar 2020 01:49:14 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb33/Debian_9.0/amd64/arangodb3-3.3.25-1_amd64.deb
# Tue, 31 Mar 2020 01:49:14 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb33/Debian_9.0/amd64/arangodb3-3.3.25-1_amd64.deb.asc
# Tue, 31 Mar 2020 01:49:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         dirmngr         gpg     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:49:28 GMT
RUN gpg --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 31 Mar 2020 01:49:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         curl         libjemalloc1         libtasn1-6         numactl         openssl         pwgen         sensible-utils     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:49:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 01:49:52 GMT
RUN curl --fail -O ${ARANGO_SIGNATURE_URL} &&           curl --fail -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf     && chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps     && chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps     &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 31 Mar 2020 01:49:53 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 31 Mar 2020 01:49:53 GMT
COPY file:01bdd453b032c9d383e66c7e6332049490bb7877724d3bb90d185f11336934d2 in /entrypoint.sh 
# Tue, 31 Mar 2020 01:49:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 01:49:53 GMT
EXPOSE 8529
# Tue, 31 Mar 2020 01:49:53 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cbfdf7be5d0a9cfc6d40d0563d715456b491845f98c74cab7bba3dd90db998`  
		Last Modified: Tue, 31 Mar 2020 01:50:52 GMT  
		Size: 6.6 MB (6566458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc110f2972991d39fab4ccd21c634317136a6d2ac764a6a26003891586473f18`  
		Last Modified: Tue, 31 Mar 2020 01:50:50 GMT  
		Size: 4.4 KB (4447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fba0aecf02ac557cc6a7b1f48320843554cab334bbf392b4bd17eeb5b1506fa`  
		Last Modified: Tue, 31 Mar 2020 01:50:52 GMT  
		Size: 7.5 MB (7461612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28339a396e65dd149e1cc7e0bdb7c2a05c69ef850a95689f6fe7ed02bf36a2d0`  
		Last Modified: Tue, 31 Mar 2020 01:50:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e62b4fd0d0980ad90d579c2247248542a7f87f18b3c9eaf64cf5b1c2a0c4bf5`  
		Last Modified: Tue, 31 Mar 2020 01:51:02 GMT  
		Size: 57.8 MB (57785314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b50b1475da0f9343fabc7ab0309cfe831d1366a1a14560bcb47880f5f57c5c7`  
		Last Modified: Tue, 31 Mar 2020 01:50:50 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.4`

```console
$ docker pull arangodb@sha256:c32bcd08a60c1da2e96b02fa8db1ac2bde22b899245a4699c6449d16fe736e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.4` - linux; amd64

```console
$ docker pull arangodb@sha256:f354f9650ae0c94def2826c2aa13b289f6007fec9d4cd575d66e2a13a591456b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101990383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8bbe8672ebba1abbf2225666e1dfc2e153874340c4fa52b0b08755e5d85ad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 25 Jan 2020 01:19:37 GMT
ENV ARANGO_VERSION=3.4.9
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_PACKAGE=arangodb3_3.4.9-1_amd64.deb
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.9-1_amd64.deb
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.9-1_amd64.deb.asc
# Sat, 25 Jan 2020 01:20:01 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 25 Jan 2020 01:20:02 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 25 Jan 2020 01:20:02 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Sat, 25 Jan 2020 01:20:02 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Sat, 25 Jan 2020 01:20:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:20:03 GMT
EXPOSE 8529
# Sat, 25 Jan 2020 01:20:03 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd71998e0104b799cecf1dc84120cc5f654bcf1b1a01fec4714dd1b9e417ca52`  
		Last Modified: Sat, 25 Jan 2020 01:20:42 GMT  
		Size: 99.2 MB (99200973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccb3bc7bf0a313e2619890c9ae7742e6e557d431b852716e5dd195d3808f442`  
		Last Modified: Sat, 25 Jan 2020 01:20:24 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1993e49cf3e237fbc357190ae1df3b0b9b49ec93e21d2e4fb7f92d762443632`  
		Last Modified: Sat, 25 Jan 2020 01:20:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.4.9`

```console
$ docker pull arangodb@sha256:c32bcd08a60c1da2e96b02fa8db1ac2bde22b899245a4699c6449d16fe736e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.4.9` - linux; amd64

```console
$ docker pull arangodb@sha256:f354f9650ae0c94def2826c2aa13b289f6007fec9d4cd575d66e2a13a591456b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101990383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8bbe8672ebba1abbf2225666e1dfc2e153874340c4fa52b0b08755e5d85ad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 25 Jan 2020 01:19:37 GMT
ENV ARANGO_VERSION=3.4.9
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_PACKAGE=arangodb3_3.4.9-1_amd64.deb
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.9-1_amd64.deb
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.9-1_amd64.deb.asc
# Sat, 25 Jan 2020 01:20:01 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 25 Jan 2020 01:20:02 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 25 Jan 2020 01:20:02 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Sat, 25 Jan 2020 01:20:02 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Sat, 25 Jan 2020 01:20:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:20:03 GMT
EXPOSE 8529
# Sat, 25 Jan 2020 01:20:03 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd71998e0104b799cecf1dc84120cc5f654bcf1b1a01fec4714dd1b9e417ca52`  
		Last Modified: Sat, 25 Jan 2020 01:20:42 GMT  
		Size: 99.2 MB (99200973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccb3bc7bf0a313e2619890c9ae7742e6e557d431b852716e5dd195d3808f442`  
		Last Modified: Sat, 25 Jan 2020 01:20:24 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1993e49cf3e237fbc357190ae1df3b0b9b49ec93e21d2e4fb7f92d762443632`  
		Last Modified: Sat, 25 Jan 2020 01:20:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.5`

```console
$ docker pull arangodb@sha256:b935728c194b217f0e7a1cb91fd35d7d638034394d2a683879a2cf0a67c7e68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.5` - linux; amd64

```console
$ docker pull arangodb@sha256:62b5c1907ccfa74533c35e299f4e868f87d2efbf2a0761f8dfc7af99e14520e6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110503803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044bb2b6b89c3b4d8bfe2a489ed097fcf0c6a5729dc26a2fdc97e435be972cff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_VERSION=3.5.4
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_PACKAGE=arangodb3_3.5.4-1_amd64.deb
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.4-1_amd64.deb
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.4-1_amd64.deb.asc
# Thu, 23 Jan 2020 17:10:18 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 23 Jan 2020 17:10:19 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 23 Jan 2020 17:10:19 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Thu, 23 Jan 2020 17:10:19 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Thu, 23 Jan 2020 17:10:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 17:10:19 GMT
EXPOSE 8529
# Thu, 23 Jan 2020 17:10:19 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b894beb4738887c1152b7d7f1549123f4b522147acd9c92006b54013e40134`  
		Last Modified: Thu, 23 Jan 2020 17:11:48 GMT  
		Size: 107.7 MB (107714396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36e3ba3ee3abb406b1eb2d88f2e4f920861b71d868af63b966e113f57b22c5b`  
		Last Modified: Thu, 23 Jan 2020 17:11:29 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded7a88e79982f58478fb0b3dddd36d284712c45855b584ed2a356730b471f91`  
		Last Modified: Thu, 23 Jan 2020 17:11:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.5.4`

```console
$ docker pull arangodb@sha256:b935728c194b217f0e7a1cb91fd35d7d638034394d2a683879a2cf0a67c7e68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.5.4` - linux; amd64

```console
$ docker pull arangodb@sha256:62b5c1907ccfa74533c35e299f4e868f87d2efbf2a0761f8dfc7af99e14520e6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110503803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044bb2b6b89c3b4d8bfe2a489ed097fcf0c6a5729dc26a2fdc97e435be972cff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_VERSION=3.5.4
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_PACKAGE=arangodb3_3.5.4-1_amd64.deb
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.4-1_amd64.deb
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.4-1_amd64.deb.asc
# Thu, 23 Jan 2020 17:10:18 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 23 Jan 2020 17:10:19 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 23 Jan 2020 17:10:19 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Thu, 23 Jan 2020 17:10:19 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Thu, 23 Jan 2020 17:10:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 17:10:19 GMT
EXPOSE 8529
# Thu, 23 Jan 2020 17:10:19 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b894beb4738887c1152b7d7f1549123f4b522147acd9c92006b54013e40134`  
		Last Modified: Thu, 23 Jan 2020 17:11:48 GMT  
		Size: 107.7 MB (107714396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36e3ba3ee3abb406b1eb2d88f2e4f920861b71d868af63b966e113f57b22c5b`  
		Last Modified: Thu, 23 Jan 2020 17:11:29 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded7a88e79982f58478fb0b3dddd36d284712c45855b584ed2a356730b471f91`  
		Last Modified: Thu, 23 Jan 2020 17:11:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6`

```console
$ docker pull arangodb@sha256:60e34a105dc96a3feed9e4587defa8b2ef5cd708c031c57818888f3f2c171ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:6d767db42f4e172e232be9b5f7558098a72a25fdf93347d7972ba8d478eba168
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110403610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9444c3cbb5ba2bef95351b0d6e5965fa6c542eab24a7f907109e1d1c7add5d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_VERSION=3.6.2
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.2-1_amd64.deb
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.2-1_amd64.deb
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.2-1_amd64.deb.asc
# Wed, 11 Mar 2020 22:20:06 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 11 Mar 2020 22:20:06 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 11 Mar 2020 22:20:06 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Wed, 11 Mar 2020 22:20:07 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Wed, 11 Mar 2020 22:20:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2020 22:20:07 GMT
EXPOSE 8529
# Wed, 11 Mar 2020 22:20:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07085b9d9386b54af56ada05173b099ef139c3c914726899b2227989e71b587b`  
		Last Modified: Wed, 11 Mar 2020 22:20:35 GMT  
		Size: 107.6 MB (107614200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d915dc20c3286fedbc6b41419a943c6e153bc27324725b9064972b921a12a3d8`  
		Last Modified: Wed, 11 Mar 2020 22:20:17 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a8b8b82fc6d9f4264ea4116370f359195a8fa697d5a313e46284009990742e`  
		Last Modified: Wed, 11 Mar 2020 22:20:16 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.2`

```console
$ docker pull arangodb@sha256:60e34a105dc96a3feed9e4587defa8b2ef5cd708c031c57818888f3f2c171ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6.2` - linux; amd64

```console
$ docker pull arangodb@sha256:6d767db42f4e172e232be9b5f7558098a72a25fdf93347d7972ba8d478eba168
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110403610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9444c3cbb5ba2bef95351b0d6e5965fa6c542eab24a7f907109e1d1c7add5d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_VERSION=3.6.2
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.2-1_amd64.deb
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.2-1_amd64.deb
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.2-1_amd64.deb.asc
# Wed, 11 Mar 2020 22:20:06 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 11 Mar 2020 22:20:06 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 11 Mar 2020 22:20:06 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Wed, 11 Mar 2020 22:20:07 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Wed, 11 Mar 2020 22:20:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2020 22:20:07 GMT
EXPOSE 8529
# Wed, 11 Mar 2020 22:20:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07085b9d9386b54af56ada05173b099ef139c3c914726899b2227989e71b587b`  
		Last Modified: Wed, 11 Mar 2020 22:20:35 GMT  
		Size: 107.6 MB (107614200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d915dc20c3286fedbc6b41419a943c6e153bc27324725b9064972b921a12a3d8`  
		Last Modified: Wed, 11 Mar 2020 22:20:17 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a8b8b82fc6d9f4264ea4116370f359195a8fa697d5a313e46284009990742e`  
		Last Modified: Wed, 11 Mar 2020 22:20:16 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:60e34a105dc96a3feed9e4587defa8b2ef5cd708c031c57818888f3f2c171ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:6d767db42f4e172e232be9b5f7558098a72a25fdf93347d7972ba8d478eba168
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110403610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9444c3cbb5ba2bef95351b0d6e5965fa6c542eab24a7f907109e1d1c7add5d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_VERSION=3.6.2
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.2-1_amd64.deb
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.2-1_amd64.deb
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.2-1_amd64.deb.asc
# Wed, 11 Mar 2020 22:20:06 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 11 Mar 2020 22:20:06 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 11 Mar 2020 22:20:06 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Wed, 11 Mar 2020 22:20:07 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Wed, 11 Mar 2020 22:20:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2020 22:20:07 GMT
EXPOSE 8529
# Wed, 11 Mar 2020 22:20:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07085b9d9386b54af56ada05173b099ef139c3c914726899b2227989e71b587b`  
		Last Modified: Wed, 11 Mar 2020 22:20:35 GMT  
		Size: 107.6 MB (107614200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d915dc20c3286fedbc6b41419a943c6e153bc27324725b9064972b921a12a3d8`  
		Last Modified: Wed, 11 Mar 2020 22:20:17 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a8b8b82fc6d9f4264ea4116370f359195a8fa697d5a313e46284009990742e`  
		Last Modified: Wed, 11 Mar 2020 22:20:16 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
