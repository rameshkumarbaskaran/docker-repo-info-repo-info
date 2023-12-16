## `mongo:5-focal`

```console
$ docker pull mongo@sha256:5ea65c3fba9b0ce3efeb168d571323f34942d9615ac3213d46ea30dbd51a3f92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:339da49b0337da248ee7c08de6261be00be696bacb917979efae53fae91d706c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265209728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68a9087e37537f3602ad20cdf253f2b9a06a6280cc2096de2e2dd7624c84d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:05:33 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:05:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:05:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:05:33 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Nov 2023 23:05:33 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Mon, 27 Nov 2023 23:05:33 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:05:33 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:05:33 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_MAJOR=5.0
# Mon, 27 Nov 2023 23:05:33 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_VERSION=5.0.23
# Mon, 27 Nov 2023 23:05:33 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:05:33 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:05:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:05:33 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:05:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999863a67ff00d298962e94cedeed4c7d79bb60b110e7dbd7e586fdec0e94844`  
		Last Modified: Fri, 15 Dec 2023 22:06:04 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52b8e5cdc476a6f0567ab16fbc7da91d025052d0013ea429029fa8a0d200bdc`  
		Last Modified: Fri, 15 Dec 2023 22:06:04 GMT  
		Size: 8.4 MB (8373143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e971e858300278f4a8ceb2194adf46cde636dc30cf85ad8d7c10cdcdb0a2d535`  
		Last Modified: Fri, 15 Dec 2023 22:06:04 GMT  
		Size: 1.1 MB (1099536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef71d8ed99b2df6372d3e98f562bc0edc96a0c06492396a086dd037a20296da`  
		Last Modified: Fri, 15 Dec 2023 22:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6c05177503fe554632dc71e91bb43027aaec8c91ae09b2b7fd6e30d13834d`  
		Last Modified: Fri, 15 Dec 2023 22:06:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81dc9b207bbe70c772746942a8e677c403f4a4d05232e08b640f61a02ac3028`  
		Last Modified: Fri, 15 Dec 2023 22:06:05 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f054589723856f1280f11d2c62f58eb69bf5368b9d6683cf468ae826115bd2f`  
		Last Modified: Fri, 15 Dec 2023 22:06:10 GMT  
		Size: 228.2 MB (228215938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28245c26cc0de6c7572502c46878af08fc1b429e3905ed66f00929ca842e534b`  
		Last Modified: Fri, 15 Dec 2023 22:06:06 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:22ef6f98a1e63be9da57e16444b835c9d04c7bdbccea0ff88afa13c782c3e85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a443520fe6f83131706dc6d51350a2201a7a6b5d9b41439fd6d5ba7bc47baf`

```dockerfile
```

-	Layers:
	-	`sha256:b03b1ca91b702519091d63cf5c3b4b9ced1ed34bd033a666ed3d1ad9816c58fa`  
		Last Modified: Fri, 15 Dec 2023 22:06:04 GMT  
		Size: 2.7 MB (2729388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6ff704a1f053c088361fdf80d4616ffd51255ac09e4771ed9abdb51ac92e68`  
		Last Modified: Fri, 15 Dec 2023 22:06:04 GMT  
		Size: 28.0 KB (28043 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:fc30f224ebd44e9ec79c34f239e6489bf72229ce47aa985b4ddbc577c72b29fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257627805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d339768a8be53059c67d4a5a7fbbccc6d0070075ca9bc67e7e318251bd0456`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:05:33 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:05:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:05:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:05:33 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Nov 2023 23:05:33 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Mon, 27 Nov 2023 23:05:33 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:05:33 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:05:33 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_MAJOR=5.0
# Mon, 27 Nov 2023 23:05:33 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_VERSION=5.0.23
# Mon, 27 Nov 2023 23:05:33 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:05:33 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:05:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:05:33 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:05:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440c3515d9bd0964d0a548e96e6c40c88bac16d79895803e445da40f75bc9c93`  
		Last Modified: Fri, 15 Dec 2023 23:16:45 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83730c7676858b876848ebb4478f4d61832d0d8454fb5e7a8478e6fcd032bdef`  
		Last Modified: Fri, 15 Dec 2023 23:16:46 GMT  
		Size: 8.2 MB (8200537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa65f7674304638cfc796894a181ba74c3d04599e1d4d32ecd66bd3924ec64b9`  
		Last Modified: Fri, 15 Dec 2023 23:16:45 GMT  
		Size: 1.0 MB (1031362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54b616871ccbec6f9d3a000e206c6a3906fdcad14920bc048d656415c93c941`  
		Last Modified: Fri, 15 Dec 2023 23:16:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90c58e97797915787e5fe507accd16531be436fdb2c8f8b01b3548cd4b7f055`  
		Last Modified: Fri, 15 Dec 2023 23:16:46 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344353b0e5c897e391f10bf23b09a86f0a339dcbe571fc15ae0cf2a397d7dd22`  
		Last Modified: Fri, 15 Dec 2023 23:16:47 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651664cd5a8f437f970db516b79bea8ae3513a4607c8b35300a84630300b3794`  
		Last Modified: Fri, 15 Dec 2023 23:16:57 GMT  
		Size: 222.4 MB (222411851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371d1da4906d4b945ac4868d2980ca1ddef96ef5dcac2a087a42dccdedba27a9`  
		Last Modified: Fri, 15 Dec 2023 23:16:47 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:7b4fbf8255f27a6209f968b1009807799f95f0bd4886a18dfef89309aeb8b62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5885164b954ffe91ce222dda7d8eb8bab84dcc8ee06eaec8584554c4baf4081`

```dockerfile
```

-	Layers:
	-	`sha256:e13bb32f18996643b2a0e0ba5e3db88d5176aa094295f5e6cac6d3fda77a9f8c`  
		Last Modified: Fri, 15 Dec 2023 23:16:46 GMT  
		Size: 2.7 MB (2729726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38deed2eeec11867ba1aa49ac2aa1ebb26217fe33d90c486941640977f25e98a`  
		Last Modified: Fri, 15 Dec 2023 23:16:45 GMT  
		Size: 27.9 KB (27897 bytes)  
		MIME: application/vnd.in-toto+json
