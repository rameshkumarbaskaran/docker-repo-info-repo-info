## `mongo:4-focal`

```console
$ docker pull mongo@sha256:dece5bcb580424f101922fe342bf8af06152f967005e82e1266eed31f073576f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:893ce9fc50512e27ad7c1d805bda6546acf6c4820279c576455124b56446a71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acbb73ce0b39cf21b917ff8e3dfc150f79b4c61536d3b331ac5627f5ce1a7c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:03:16 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:03:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:03:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:03:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Nov 2023 23:03:16 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Mon, 27 Nov 2023 23:03:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:03:16 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:03:16 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_MAJOR=4.4
# Mon, 27 Nov 2023 23:03:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_VERSION=4.4.26
# Mon, 27 Nov 2023 23:03:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:03:16 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:03:16 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:03:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c56ef422c2ca735fc33ceeced36fa10ee4320a5245bb85c67c2d4601ef1bf7c`  
		Last Modified: Fri, 15 Dec 2023 22:05:45 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c577f863c7fa31deb13c1e0afad22204fc74f9c37a74e1cd9dcfade166342df8`  
		Last Modified: Fri, 15 Dec 2023 22:05:45 GMT  
		Size: 8.4 MB (8373208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6deb6675a2dba8b6dfa3edbaf4ccfdb63c27d8333e461374dc48bd9fbaf6973`  
		Last Modified: Fri, 15 Dec 2023 22:05:45 GMT  
		Size: 1.1 MB (1099523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b71e1c72f3da606dac7a76f2f6643c81e3cf5af8f8b57bc13946f9830d08ca8`  
		Last Modified: Fri, 15 Dec 2023 22:05:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2386a58dcc2866546c1005eb4f633b62e6653bdc95864c97a789f724979c28f9`  
		Last Modified: Fri, 15 Dec 2023 22:05:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945e0aef512ae8b318039c8178c7b4158caaaa655b3628162ad534ecc9e18e92`  
		Last Modified: Fri, 15 Dec 2023 22:05:46 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2f6c52606b752165f2dd8f49048e8f2cca700323bfb08662a393febfe716b`  
		Last Modified: Fri, 15 Dec 2023 22:05:49 GMT  
		Size: 139.3 MB (139274274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56b64d51f3202ba3ce1d43733047d0031ffe1dbd26216a8d30e874da0470c32`  
		Last Modified: Fri, 15 Dec 2023 22:05:47 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:b1fa497f6d9341eb707b177e546093dc85e9956f3e3aefa0cfb65ffb2ddb31c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2619c933db797d2b71896fa5413367fa655938b6231b237260197d974d7976e`

```dockerfile
```

-	Layers:
	-	`sha256:c33e1a59849866a7b64ebaf88e76df9b2de462712ef51cfc79a53e1dbf182f92`  
		Last Modified: Fri, 15 Dec 2023 22:05:45 GMT  
		Size: 2.7 MB (2723946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55132c5443b56ed2237aa822a8409e19ee5ae95596b98820768bd6ef5290b6c5`  
		Last Modified: Fri, 15 Dec 2023 22:05:45 GMT  
		Size: 28.0 KB (28043 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ceac3e35413f462020b6b5ea215f53377ec78a7cea01c8645b129d5806f362b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171507420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb856fcc681bb144d92ce2b6023f9f0fc3bbcf1b3d9494e2035130edda7b9ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:03:16 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:03:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:03:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:03:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Nov 2023 23:03:16 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Mon, 27 Nov 2023 23:03:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:03:16 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:03:16 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_MAJOR=4.4
# Mon, 27 Nov 2023 23:03:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_VERSION=4.4.26
# Mon, 27 Nov 2023 23:03:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:03:16 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:03:16 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:03:16 GMT
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
	-	`sha256:1006dff9a1f8f3342351d0ef9bc8f05265edfdf4436a8b9f00e3224b42acb41f`  
		Last Modified: Fri, 15 Dec 2023 23:18:33 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667c5f38a263e0518bb5ea807fba03e5c4eee652f07b8be419072852cb17dfb5`  
		Last Modified: Fri, 15 Dec 2023 23:18:33 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b2ff9465cd2137e6ca447f3e91107b6e847e58ef2820bc7a3d8b33f422d68a`  
		Last Modified: Fri, 15 Dec 2023 23:18:41 GMT  
		Size: 136.3 MB (136291464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2445e472bd822531e844f2f79b0772f736d4eed05dc06af5e5c98a5d18f8bf02`  
		Last Modified: Fri, 15 Dec 2023 23:18:33 GMT  
		Size: 5.0 KB (4994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:1aa135122afa6c26b6abb9a908afd3d3d1a9d215cb6d17fb1276612aecc08ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a045f209008da407c82ffd1085d06c6d1bb405c3e190369ca8f7196287a3dea`

```dockerfile
```

-	Layers:
	-	`sha256:ed0045a5cd5b6b08a3c805b0d22190b0a83272a90d2f7da5f8682232e036e854`  
		Last Modified: Fri, 15 Dec 2023 23:18:33 GMT  
		Size: 2.7 MB (2724284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed08bd35e2b08c04329243dccb49cc6bf76609320481cca668d8f8f0847c8a4c`  
		Last Modified: Fri, 15 Dec 2023 23:18:33 GMT  
		Size: 27.9 KB (27896 bytes)  
		MIME: application/vnd.in-toto+json
