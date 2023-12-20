## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:b4f4b5157181e5fab4b61a7971a85c7b98e5bde7cffc668087ef5557008113a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:fbf99c82b3774b06aec63ddc9439daef04824171583d1ed8edda63fcd251d4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247634418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5c2fe902ada88825e6b986021977cdcdf18923923c5e3c9b2c7fe928559124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV GOSU_VERSION=1.16
# Tue, 19 Dec 2023 19:08:50 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_MAJOR=6.0
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_VERSION=6.0.12
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
VOLUME [/data/db /data/configdb]
# Tue, 19 Dec 2023 19:08:50 GMT
ENV HOME=/data/db
# Tue, 19 Dec 2023 19:08:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 19:08:50 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 19 Dec 2023 19:08:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a486411936734b0d1d201c8a0ed8e9d449a64d5033fdc33411ec95bc26460efb`  
		Last Modified: Tue, 12 Dec 2023 11:55:25 GMT  
		Size: 29.5 MB (29547485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0c419a0ab4b370b5bc788f96640219b8be9044e8d33d22b819947333553db4`  
		Last Modified: Wed, 20 Dec 2023 20:14:17 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae9ec9a6c84e4fd9161845858a863b867d0f88092ac58e76d617fec304899a`  
		Last Modified: Wed, 20 Dec 2023 20:14:17 GMT  
		Size: 5.0 MB (5049090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abeba89c4f2b88394835500f9010659b5d7a74a2b99adbf9aabd0a01be7c02c`  
		Last Modified: Wed, 20 Dec 2023 20:14:17 GMT  
		Size: 1.1 MB (1101002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36691189d2b33e61c35bf6e47d1873548c49a1ac7cd46be34ac4e5368f5c6c7`  
		Last Modified: Wed, 20 Dec 2023 20:14:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586188b51ee3d6400f1d22b2cac03e1b05f8abaf9833da1932c1459035caac14`  
		Last Modified: Wed, 20 Dec 2023 20:14:18 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4cb0b39af2fa15f30c38c4c41d9625a27ec58c2f654ac75cce96f9d3f68104`  
		Last Modified: Wed, 20 Dec 2023 20:14:18 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce183a11563668be7e868cf70b8e3ca701e301262ede51e88efca30480ec8545`  
		Last Modified: Wed, 20 Dec 2023 20:14:23 GMT  
		Size: 211.9 MB (211928275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9cc3c0de71bceac2c627786edf02a81013852adce6b9ee1c0744083565b65f`  
		Last Modified: Wed, 20 Dec 2023 20:14:19 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:c2706677502a536947633ba4be1fa36e53474a6e0e5cb5828b0577d0ee5ef8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e54fe80f6ed0ee5c182f31881d37893b530c7543d88827c71aef24591bc9231`

```dockerfile
```

-	Layers:
	-	`sha256:1bea8a4aa852b052e6b0d6076d06881d19f68820ab62dee476ce3025fea36492`  
		Last Modified: Wed, 20 Dec 2023 20:14:17 GMT  
		Size: 2.7 MB (2728094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb8044d3641d8c3563aa00e06c71ace6b39a27a36a2231fce3f66e1e84a7c7f`  
		Last Modified: Wed, 20 Dec 2023 20:14:17 GMT  
		Size: 28.9 KB (28941 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:debb375a561f5782939eea313a68841ed55e3a2ea35bb79f13c559a4445d0399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240489299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2aabe98651eb56ac73f2ced179364eec30c674343fbf13428d2c2d94201fd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV GOSU_VERSION=1.16
# Tue, 19 Dec 2023 19:08:50 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_MAJOR=6.0
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_VERSION=6.0.12
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
VOLUME [/data/db /data/configdb]
# Tue, 19 Dec 2023 19:08:50 GMT
ENV HOME=/data/db
# Tue, 19 Dec 2023 19:08:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 19:08:50 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 19 Dec 2023 19:08:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:005e2837585d0b391170fd9faf2e0c279d64ba0eb011cda8dedf28cb5839861e`  
		Last Modified: Tue, 12 Dec 2023 11:55:31 GMT  
		Size: 27.4 MB (27358237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60b3ed21100ca2d890876fbf18f05af88846ecbf268dc5e5a49ce0438d31830`  
		Last Modified: Sat, 16 Dec 2023 21:11:13 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fcf60fea85148cf8db272596d20236398f26e0a280d8cec374de81aa444e97`  
		Last Modified: Sat, 16 Dec 2023 21:11:14 GMT  
		Size: 5.0 MB (4992669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05da3aee34af09b4d42d3f493c4227bc34d568cf8f4b2f78f030e25bf7dd43f7`  
		Last Modified: Wed, 20 Dec 2023 22:07:31 GMT  
		Size: 1.0 MB (1034220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f2bf503f3292952c7caabc35876274ecfcaf7bb99db01a8a0b85769a553daf`  
		Last Modified: Wed, 20 Dec 2023 22:07:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0c9f5de7641176841ad3415ae418e07cc9aba99b65cde469da37a8bb93c2d9`  
		Last Modified: Wed, 20 Dec 2023 22:08:33 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88fa6fbb418c8d016b72ee31181b96d53ef3c503aaef2272fab8f857406bb9`  
		Last Modified: Wed, 20 Dec 2023 22:08:33 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dfa90afa9389c01d7124622d60724b91c42033b6b6d8f098d03419efef4a78`  
		Last Modified: Wed, 20 Dec 2023 22:08:41 GMT  
		Size: 207.1 MB (207095592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73309f9bc7199b4005b2fe30896d7f1754a9e2ea9718f4caf32aa30dd4aba197`  
		Last Modified: Wed, 20 Dec 2023 22:08:34 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:d67043526cfd1903571c4ef69bbd438f2945ae64c5bde1afcc93b9efeaf7eec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2f1ad27d5f3df22c63d4dad20496fc1734666fa0979d790af673cea1362c89`

```dockerfile
```

-	Layers:
	-	`sha256:0ab3a9fef68298d1285f1073836242979b88c80c71ce8afb1a9d33325e2c4013`  
		Last Modified: Wed, 20 Dec 2023 22:08:34 GMT  
		Size: 2.7 MB (2728452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f76e946bc437519f09e76416e4d81c96d993c04c986dbc4cc39a766902061b`  
		Last Modified: Wed, 20 Dec 2023 22:08:33 GMT  
		Size: 28.8 KB (28792 bytes)  
		MIME: application/vnd.in-toto+json
