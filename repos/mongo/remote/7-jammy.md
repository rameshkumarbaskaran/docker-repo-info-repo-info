## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:c8c45af5a1105bb57fb11ce12867c7af94c30e1a652b168e50b71b6feaaf4a3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:6030f098b30d90c3351b231ca02446c66a8863dfc24af058bb41125f004a3839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260103179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acc6a2b3549a15026a95f7614a93f8cfc361031bdd22034d14e7080ca7d064e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:12:52 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:12:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:12:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:12:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Nov 2023 23:12:52 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Mon, 27 Nov 2023 23:12:52 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:12:52 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:12:52 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:12:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:12:52 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:12:52 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:12:52 GMT
ENV MONGO_MAJOR=7.0
# Mon, 27 Nov 2023 23:12:52 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
ENV MONGO_VERSION=7.0.4
# Mon, 27 Nov 2023 23:12:52 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:12:52 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:12:52 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:12:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5e8117c0bd28aecad06f7e76d4d3b64734d59c1a0a44541d18060cd8fba30c50`  
		Last Modified: Fri, 01 Dec 2023 08:21:32 GMT  
		Size: 29.5 MB (29547417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0854a1b932a4fe6d68c535ab3fd2ca321f1066d3c2c6844800c5848e63d95d39`  
		Last Modified: Fri, 15 Dec 2023 22:06:09 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6429ddbd6cd1e80c26a91a15bcaa30fdeea9a15a80e5f9f62ef68c39ba11fb79`  
		Last Modified: Fri, 15 Dec 2023 22:06:10 GMT  
		Size: 5.0 MB (5049051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a51492dc7482de39185272be33636420dad045545cf365078839ce7117caf7`  
		Last Modified: Fri, 15 Dec 2023 22:06:10 GMT  
		Size: 1.1 MB (1100106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f76241c3ba5efb62978aaea37b0d4b036727729878d017e43a08d6d10c52525`  
		Last Modified: Fri, 15 Dec 2023 22:06:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d74062c396d4ea127af15e721804448cefd17867ea64a5a983a95acd2f6538`  
		Last Modified: Fri, 15 Dec 2023 22:06:11 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e96aeb2c644aac4935a307d17953489aac4caa125ca1a551bed049e7483d22`  
		Last Modified: Fri, 15 Dec 2023 22:06:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269b9732391ec0df116f12688cbf9da549ed38159773dd86f9da03e0cac1d536`  
		Last Modified: Fri, 15 Dec 2023 22:06:18 GMT  
		Size: 224.4 MB (224398039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1676831104b84d439ceb213a0db915ca7887f98be96c5a279051f5415635bc0`  
		Last Modified: Fri, 15 Dec 2023 22:06:12 GMT  
		Size: 5.0 KB (4994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:be78e6a4e439d497957e073802c9912229cbf34340c6bb1942ff807b727860d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2756465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0549a0218643008a2c05adcd92d0033bef8ee326623c48c60dd8df8ab731b4a7`

```dockerfile
```

-	Layers:
	-	`sha256:baaad11d06ad31c9f7c8612130a1f7a2ae128908908c0272138917fd8a82424d`  
		Last Modified: Fri, 15 Dec 2023 22:06:10 GMT  
		Size: 2.7 MB (2727518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f7ce787f0bdf6476ad792744de7c01e31f02722e3ae351d11ac6ebc2d4dd04`  
		Last Modified: Fri, 15 Dec 2023 22:06:10 GMT  
		Size: 28.9 KB (28947 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a25392a70f42d2e6d4b24a10919f9289762fd367cb813dbe235261b026f224c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251972562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1fda32d4fd045c2d24a6681d4d1d3f3e7614f860d59ffce8d4ae1e9ad3570a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:12:52 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:12:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:12:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:12:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Nov 2023 23:12:52 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Mon, 27 Nov 2023 23:12:52 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:12:52 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:12:52 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:12:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:12:52 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:12:52 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:12:52 GMT
ENV MONGO_MAJOR=7.0
# Mon, 27 Nov 2023 23:12:52 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
ENV MONGO_VERSION=7.0.4
# Mon, 27 Nov 2023 23:12:52 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:12:52 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:12:52 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:12:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:32ba3a3141d26dce5dc8f42b11b36e32f5986433d380291ba7f98b143af3fc46`  
		Last Modified: Fri, 01 Dec 2023 08:21:38 GMT  
		Size: 27.4 MB (27357622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d9bdd566eda8119ecd9130fbe410040a52fc0aebbedfc1e97039b522dcc6c0`  
		Last Modified: Fri, 15 Dec 2023 23:13:29 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12519bfabd2f3f02601fa51e69d31b325581d1d7dd2f03b165d0742c26342be3`  
		Last Modified: Fri, 15 Dec 2023 23:13:30 GMT  
		Size: 5.0 MB (4992338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b66d94654416702317917cb649d256abdf80769c0ab6722a8d5e95972556e`  
		Last Modified: Fri, 15 Dec 2023 23:13:30 GMT  
		Size: 1.0 MB (1033095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c4a3bc7371d85c83d97d28bb1f1559adf331fbce852c18510cb677651b04a`  
		Last Modified: Fri, 15 Dec 2023 23:13:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f78bc84731b0345712b8f2b6f7d20226f1e88b05f8acfe5bcb6dbe91e32b1b`  
		Last Modified: Fri, 15 Dec 2023 23:13:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d924d95321d28cfade4894c8607a9b594743e8b2629c0a5d7fa7da22c7c4e098`  
		Last Modified: Fri, 15 Dec 2023 23:13:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c3ff737830dc85ee4a23ab777c6d6587c6a837d93f9fec3cd4d4d78002cde6`  
		Last Modified: Fri, 15 Dec 2023 23:13:37 GMT  
		Size: 218.6 MB (218580942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028ee93db7672a96dc1f89dc77f93fceff0fe57b3bfc2bf34097d1092afecc04`  
		Last Modified: Fri, 15 Dec 2023 23:13:32 GMT  
		Size: 5.0 KB (4992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:1e8a4bf598831d9fecd97df1be23738ed041a13e339a2f18e6a6ebaff7ebcd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2756683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d52a25a4f1025d9f93c26b213aea46d5de5d45226fb0f2b22d19209d1b390a`

```dockerfile
```

-	Layers:
	-	`sha256:09852a7c6712fc7ca367068736cf6e528ebde6003e0fd8c4bc47b6da4a2f9701`  
		Last Modified: Fri, 15 Dec 2023 23:13:30 GMT  
		Size: 2.7 MB (2727880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215fea3ca77ce3debeff208e7243ef3bc92b2e5da8ee71b935c910d179eb2d71`  
		Last Modified: Fri, 15 Dec 2023 23:13:30 GMT  
		Size: 28.8 KB (28803 bytes)  
		MIME: application/vnd.in-toto+json
