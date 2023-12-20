## `mongo:jammy`

```console
$ docker pull mongo@sha256:c78d986621978547187d5c514392fda374c25ea7b335a3eecfe6d22c8c12cd06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:5cac0ca634f0932298bac9b2cfe6a9d9161b7e501a551bd9a6aae8c90308cfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260105620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e123a0ccb4bac0a293ad45cf5f38091c048e6cf2d691ff49d0b905f34f409c9`
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
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_MAJOR=7.0
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_VERSION=7.0.4
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
	-	`sha256:bf55b1330fcad2a1b217d2dcc3fca9be38e8cb09bf5fc7e1e34160e36013b411`  
		Last Modified: Wed, 20 Dec 2023 20:13:23 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc53a6d6fe44a60e2374857148bb2744fa15b47a1d60f0a2c0a6c4bae46936`  
		Last Modified: Wed, 20 Dec 2023 20:13:24 GMT  
		Size: 5.0 MB (5049132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b429365d99b94f518123189f30f8c38428e27ff79bb80f213e1a309627619ced`  
		Last Modified: Wed, 20 Dec 2023 20:13:24 GMT  
		Size: 1.1 MB (1101006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7bc11665820b6cdfc7e4cc87da47245f1a9dc317f433a97ae5b23729d6c884`  
		Last Modified: Wed, 20 Dec 2023 20:13:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261b4f40ad6be311f11c4c018cdb852dd61f26cdfac0a33e71cbddf18a98fc20`  
		Last Modified: Wed, 20 Dec 2023 20:13:24 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d4b3f3d31c4b6b33c96c82ce1a60ab0329635b8762eacf3e04c24fd5171845`  
		Last Modified: Wed, 20 Dec 2023 20:13:24 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60dd40f133c6237b9336c74eff390cfd974a9f787351ad2a2a32601c8adecc6`  
		Last Modified: Wed, 20 Dec 2023 20:13:28 GMT  
		Size: 224.4 MB (224399430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13e71e4c172b3144631a107b9ca35b4ffccb02b45faece7911aca1a0b2ead8`  
		Last Modified: Wed, 20 Dec 2023 20:13:24 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:10f3cc44826f459e8d2c0d68c353fe7e00c4aaa0c4f9c316af8c201f4f1e5caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea86db54467c10a5173c6a4d371f3342a09227271f03ef089e587443cb9ff23`

```dockerfile
```

-	Layers:
	-	`sha256:d23fbc1dc813a3924ab62aaaff2db691a268aafd94e9dc16b707ace5eecf19a2`  
		Last Modified: Wed, 20 Dec 2023 20:13:24 GMT  
		Size: 2.7 MB (2728666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc269f93d4b2a2dcedf054798e2aaf66fe1673a4a5cffd8a3717745850e739c`  
		Last Modified: Wed, 20 Dec 2023 20:13:24 GMT  
		Size: 29.5 KB (29526 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:134b6b20018a0063b3fe47815509f831c8387231eed0424b14b389be21f7616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251975797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c7466a395d1731ee3c2d70aa96849a3677a7df9a9ad7118452e72534cd41d4`
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
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_MAJOR=7.0
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_VERSION=7.0.4
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
	-	`sha256:e7e4d672dd05819ee13c1f7a322f1561438e1546bd44102d683fa47c120195dd`  
		Last Modified: Wed, 20 Dec 2023 22:07:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bc5c1505579051eaf1b474fb0494f6f67210f3a472eae4e81673a680766cd8`  
		Last Modified: Wed, 20 Dec 2023 22:07:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c174931be5181e5a3ca106d029314a17e4e5f3a379593f5462dc86fe717fa7c`  
		Last Modified: Wed, 20 Dec 2023 22:07:38 GMT  
		Size: 218.6 MB (218582089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500987cab84a70bd86ce2b96a1d6cda7525156723135593462cc72acbfd4c951`  
		Last Modified: Wed, 20 Dec 2023 22:07:32 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:7e881e3031e6cbe2a8487a16f230ef9528555e4c0696687987f4e2baf574b232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32463ade438f9be64c3741155ed6e532a70d6d5fac044f9a836b949e3d452bd7`

```dockerfile
```

-	Layers:
	-	`sha256:98ccc96c6af9a2b9b9a7645094d28f53857daa358b5e7d2081b5c98cd9feb7c7`  
		Last Modified: Wed, 20 Dec 2023 22:07:32 GMT  
		Size: 2.7 MB (2729028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc14794d9e0bdfd830ff7f358861b7de41a6e42ab9c02dfaaf4ec1f8ff75e78f`  
		Last Modified: Wed, 20 Dec 2023 22:07:31 GMT  
		Size: 29.4 KB (29383 bytes)  
		MIME: application/vnd.in-toto+json
