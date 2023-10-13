## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:d678f4d475877ccfd3d827a77158222748a44362c12f8d39c028ef730abaf382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:075e0577e2989efee25f8e6cd615ae1ce84da1f8c79adc3557aaf253dbf7a5e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258555294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3b4d1239f12b094c4936dd08a2fbc227300beaf784c46c509e2f1ac5e6d879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:46:00 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 13 Oct 2023 04:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:46:11 GMT
ENV GOSU_VERSION=1.16
# Fri, 13 Oct 2023 04:46:11 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 13 Oct 2023 04:46:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 04:46:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 04:46:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 04:46:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 04:46:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 04:46:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 04:46:22 GMT
ENV MONGO_MAJOR=7.0
# Fri, 13 Oct 2023 04:46:22 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 13 Oct 2023 04:46:22 GMT
ENV MONGO_VERSION=7.0.2
# Fri, 13 Oct 2023 04:46:47 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 13 Oct 2023 04:46:48 GMT
VOLUME [/data/db /data/configdb]
# Fri, 13 Oct 2023 04:46:49 GMT
ENV HOME=/data/db
# Fri, 13 Oct 2023 04:46:49 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Fri, 13 Oct 2023 04:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Oct 2023 04:46:49 GMT
EXPOSE 27017
# Fri, 13 Oct 2023 04:46:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a7480baa9dd203af7b88b2fe7e6b4f81563a7ffb540e462456ae061accb837`  
		Last Modified: Fri, 13 Oct 2023 04:49:41 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9301fbd7df07e1041efa8f0b71daef6163a40cddd61abd63c7622c0031ee4c`  
		Last Modified: Fri, 13 Oct 2023 04:49:42 GMT  
		Size: 5.1 MB (5050516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4470f2e90f14923cd6b6c2b4c9482ab700e2ee6adb23b5509826a2994aec9c`  
		Last Modified: Fri, 13 Oct 2023 04:49:42 GMT  
		Size: 1.3 MB (1252869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d046ff8fd3271879d2f76a64b0ff765e3b484eb8c712dbab9ba3f3aae73de6`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e062d62b861ed7136f7640c09410c619e0b146c7ea00bbc076ede8ffe17a2428`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72919e34fde8aa9d4c9919b131ea251cd24f66df9b967a3e9a00fcb931a80f37`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab22810dfc64751f7a29ccea57a984c2837682696e2968cc2b70d2dec140b4df`  
		Last Modified: Fri, 13 Oct 2023 04:50:06 GMT  
		Size: 221.8 MB (221804116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb05c29fbdf5fc9784b0a64980119ff3d0af61d4b325435c7be20e6d558a884d`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:73d8c0c50299e87651443b44c296827e30dee94af986f94571d85ca7eba1a839
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250434515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b10e7ef02081409e232661b3a0be9178cd8af9702c52f02cc3e746ba819a7ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:07:59 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 13 Oct 2023 05:08:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 05:08:12 GMT
ENV GOSU_VERSION=1.16
# Fri, 13 Oct 2023 05:08:12 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 13 Oct 2023 05:08:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 05:08:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 05:08:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 05:08:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 05:08:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:22 GMT
ENV MONGO_MAJOR=7.0
# Fri, 13 Oct 2023 05:08:22 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 13 Oct 2023 05:08:22 GMT
ENV MONGO_VERSION=7.0.2
# Fri, 13 Oct 2023 05:08:41 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 13 Oct 2023 05:08:45 GMT
VOLUME [/data/db /data/configdb]
# Fri, 13 Oct 2023 05:08:45 GMT
ENV HOME=/data/db
# Fri, 13 Oct 2023 05:08:45 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Fri, 13 Oct 2023 05:08:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Oct 2023 05:08:46 GMT
EXPOSE 27017
# Fri, 13 Oct 2023 05:08:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53942a81bbed58a041019d02afca8f39cb3b5fc0b340c05513ba233089ddaa64`  
		Last Modified: Fri, 13 Oct 2023 05:11:43 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c77c1ea6f8e184bfebf5bd44a67db789f6dda84d9e1765f88df461c6fc366ba`  
		Last Modified: Fri, 13 Oct 2023 05:11:44 GMT  
		Size: 5.0 MB (4993892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ffa19aee38fa5d40fbbb7ad0fed2cd802350b3e0859506d008678f433b01`  
		Last Modified: Fri, 13 Oct 2023 05:11:43 GMT  
		Size: 1.2 MB (1186372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae10bad01057285cb468c4b8ac16543be6f76dd7617e0a1dd477c7cab4e8265`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208482253dd3d9820726079a672df6e91e9b83c81c36d5554103f854670ccfc1`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beb4a4f2118534d26af685b92befcd861724f9f1ce3cd9a0cfabfecfe1452df`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ec439e9d10a9a438e985d3b2cc51b9b347fc18671ac0c3be0bec42b005dda0`  
		Last Modified: Fri, 13 Oct 2023 05:12:00 GMT  
		Size: 215.9 MB (215853631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec0210a426e8383ae429ca1af87fef7322bae1f996cd6ec11b90a132bc400de`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
