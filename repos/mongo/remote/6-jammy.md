## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:99efdafca5d812ef352995fe233a3b467a5368643175c45902535a359f88edd2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:57cf08f29e4731a67397f1a4b0b560ee24dac26ec164227886ec9b5a22766970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247632383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a5f464027c9718d34c0afdfff6acd16ecc57965c559e99128dd1c4beb84357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:09:06 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:09:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:09:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:09:06 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Nov 2023 23:09:06 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Mon, 27 Nov 2023 23:09:06 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:09:06 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:09:06 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:09:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:09:06 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:09:06 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:09:06 GMT
ENV MONGO_MAJOR=6.0
# Mon, 27 Nov 2023 23:09:06 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
ENV MONGO_VERSION=6.0.12
# Mon, 27 Nov 2023 23:09:06 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:09:06 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:09:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:09:06 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:09:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a486411936734b0d1d201c8a0ed8e9d449a64d5033fdc33411ec95bc26460efb`  
		Last Modified: Tue, 12 Dec 2023 11:55:25 GMT  
		Size: 29.5 MB (29547485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c95ac3bc2f38a7e4339ffe4bc317e2ee518a9c6dab60c58090a6074d505cf6`  
		Last Modified: Sat, 16 Dec 2023 10:49:48 GMT  
		Size: 1.8 KB (1779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ae5fa6eb237e0e4f1551fd8762a256fabc46c400d60dd490c53c58a7547d3d`  
		Last Modified: Sat, 16 Dec 2023 10:49:48 GMT  
		Size: 5.0 MB (5049083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8225365496e248edbd6f8cd423ad669f1ed53daa3ceea8c71a1ce1bbfab5dbd1`  
		Last Modified: Sat, 16 Dec 2023 10:49:48 GMT  
		Size: 1.1 MB (1100101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea24b074cb370240e0efc6951c8aa9d490427c17863f45ffec355e139957ccf7`  
		Last Modified: Sat, 16 Dec 2023 10:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e47541b4e21774b1202fb0769f7e329a9b026b28311580566f8b442108e5abd`  
		Last Modified: Sat, 16 Dec 2023 10:49:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d9fc5fd7aaf5607df4f6239e5b73c75a121c140fcd883eaddaad064d137383`  
		Last Modified: Sat, 16 Dec 2023 10:49:49 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c7fcdd6cd86c8d9b757732d194b54cdab0bc7aeedbfba58e181619ef3768f`  
		Last Modified: Sat, 16 Dec 2023 10:49:54 GMT  
		Size: 211.9 MB (211927160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157b1617b33b0cf15efcd801697f5892fe6ce6e8c0ffc3474b698796978870b`  
		Last Modified: Sat, 16 Dec 2023 10:49:49 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:047fc1221c826ecaf78c5d640acf60bd499b84ccb2c66156af946831e9f90b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2755312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048e01f75735a53e9d1ae9b4a6f0bdb1139afefa96d91109c0b5b20a82b2c31a`

```dockerfile
```

-	Layers:
	-	`sha256:404923d0938856750d411ca8341d65ff6de9053e80e8c567ef60fb7833583810`  
		Last Modified: Sat, 16 Dec 2023 10:49:48 GMT  
		Size: 2.7 MB (2726946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6efca2a908ee16ebae2a47d5170e2690c8e49c63b1317e5dcb988c567c87e6`  
		Last Modified: Sat, 16 Dec 2023 10:49:48 GMT  
		Size: 28.4 KB (28366 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:3dbe8853c94da3c23158932cf13e072c2af1d79058d1ac6a2fe17746d05dcb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240487568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a507e8e83979a2159079b74c9169afefe0e248b17e2375fe6d3f2cdd02ba94a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:09:06 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:09:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:09:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:09:06 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Nov 2023 23:09:06 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Mon, 27 Nov 2023 23:09:06 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:09:06 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:09:06 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:09:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:09:06 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:09:06 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:09:06 GMT
ENV MONGO_MAJOR=6.0
# Mon, 27 Nov 2023 23:09:06 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
ENV MONGO_VERSION=6.0.12
# Mon, 27 Nov 2023 23:09:06 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:09:06 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:09:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:09:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:09:06 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:09:06 GMT
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
	-	`sha256:ea5bd96d017e770fa20858d21c9c39a15269826802068af51d0a95149e5d05d4`  
		Last Modified: Sat, 16 Dec 2023 21:11:13 GMT  
		Size: 1.0 MB (1033354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08ff5e0599a763ba94f89ec04daff34471e6955987dbfb0d6878dd49a225645`  
		Last Modified: Sat, 16 Dec 2023 21:11:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83f8958c0fea45f6b51f467dbfbf56b921aaed29651ab337ffd5f304d1235e4`  
		Last Modified: Sat, 16 Dec 2023 21:12:15 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e13a2314abd82997cd48a1115ecbbcca85d8e41e8b812d40e0032a1bacea8e`  
		Last Modified: Sat, 16 Dec 2023 21:12:16 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a150a72af86cc6a3e4397708f908e6fc0cc645a62fadcc56c2bcb9e32984d6`  
		Last Modified: Sat, 16 Dec 2023 21:12:21 GMT  
		Size: 207.1 MB (207094729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256bfb99873c064a770c1f1ca1aa8bfc900aec63bc5096bc97a51899edf76a61`  
		Last Modified: Sat, 16 Dec 2023 21:12:16 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:55669229eb6d672321919f15f0b1a87988bbcc6d989d73ae869f82d4fcdd9b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2755523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41734c86ad41494d1c4b7c4b33d3a6e246900b75ac934280b3ab5ea7dfcc4e8`

```dockerfile
```

-	Layers:
	-	`sha256:3afdce621d5ca3bdba0949c2bbf18fb3812f144e422d694325c6af0f827dffb2`  
		Last Modified: Sat, 16 Dec 2023 21:12:15 GMT  
		Size: 2.7 MB (2727304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ca2b813f50f23f644c2cab54c4c2a1ff77a2ae5685a00ff7269e24def106f2`  
		Last Modified: Sat, 16 Dec 2023 21:12:15 GMT  
		Size: 28.2 KB (28219 bytes)  
		MIME: application/vnd.in-toto+json
