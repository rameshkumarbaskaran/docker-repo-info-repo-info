## `mongo:4-focal`

```console
$ docker pull mongo@sha256:7d2fa33f0bb81e40ab569126eb403dbf6b1ce53d50a72fbebde8243103d7f0d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:6fa73df89e75b56cb03f6dd0fd32d0bb66f22beb017e29e265606bd1d904afed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176269458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04ee971f462a2fd913c99b2fbf37af04b322cb880ee6738d615512747e024b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
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
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_MAJOR=4.4
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_VERSION=4.4.26
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
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
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34ad669ced256fe78d4b3bad11fe91ef700e82a0b896f78f1476f354755fff`  
		Last Modified: Wed, 20 Dec 2023 20:13:37 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edce3a7bf66d752f254f22df8f14fe680a8f467555d1c498198bf128cba882db`  
		Last Modified: Wed, 20 Dec 2023 20:13:37 GMT  
		Size: 8.4 MB (8373046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8558779d828f975c71b6971db049eadbf4d350e9f2f2d00268ad06329331e3`  
		Last Modified: Wed, 20 Dec 2023 20:13:37 GMT  
		Size: 1.1 MB (1100516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58be47cce42e84c444be914bdb7e53a33372b77ce64e7422b91819b956c79a26`  
		Last Modified: Wed, 20 Dec 2023 20:13:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97a13fc41637d6d12722dec7ffdb125b12adb0876de66980546981c18678701`  
		Last Modified: Wed, 20 Dec 2023 20:13:38 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8fa8a6ef2cfadfabcdb85e1c990c3a7ce6318fb938d18fa50f4615e982e2f6`  
		Last Modified: Wed, 20 Dec 2023 20:13:39 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc23456fb5a61c3a550d8406c8eb3c0adff1ca97e394135419c5f8b7b588cd`  
		Last Modified: Wed, 20 Dec 2023 20:13:42 GMT  
		Size: 139.3 MB (139274570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56b989b2c6fb94a84b342a745771ed4e6dfd2959f94f7e116352b9768871a82`  
		Last Modified: Wed, 20 Dec 2023 20:13:39 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:4b2cb42416ee060d191215b73a4cf65be01f6cbda3f9fa9638c94d07e1fed8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03cdc29a2445969d96fe7f29be3bbaae5f8807f704e710ff8f0ab72032ce6b63`

```dockerfile
```

-	Layers:
	-	`sha256:b66cc47bb2ef1c3f65d14be0aeea8658c702f58c98d7b86a871b45a911f373f3`  
		Last Modified: Wed, 20 Dec 2023 20:13:37 GMT  
		Size: 2.7 MB (2725094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b66ada01b12bec3d23fef03a29cd14bd62cd899821ba84d18349701aaeeb5ef`  
		Last Modified: Wed, 20 Dec 2023 20:13:37 GMT  
		Size: 28.6 KB (28619 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:73f5acb6281c74da4051325cb4bb263691f65979ebed395ac74393ff0ca29569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171506591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6c1472808c66d9a7be865b4a01ef23943c1f72bf2f256a5a942ad9cbfb2c63`
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
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
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
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ba6b7451f9d95719ad43508919c914407cf286d0b7fb6e1ee9a02cd51b045`  
		Last Modified: Mon, 18 Dec 2023 19:51:47 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ded41913893fb2c19b7f6cb4b21f0e12639a543c69be1d62dbe3afdf3fbc42`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 8.2 MB (8200494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deddfd4aa405910f1def1dd6fb5da28c8c01831f20100c68ba672328228d629`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 1.0 MB (1031331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae6f8162365a2edd63c6252640611da17bb92f5172d0303262b4f9b68dd2c79`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d44bb34ad2e96a269000b39df9fd446d88b5053e7c0807719affad21b0679`  
		Last Modified: Mon, 18 Dec 2023 19:51:49 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240797f3b77993b21aab5895af98ba95e3d4daedf97a2abb4e5966cfc70fe93a`  
		Last Modified: Mon, 18 Dec 2023 19:51:49 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd611e2a8a7d1a271c170167ffc8b0d124e7c0007960fe008fa0545950475781`  
		Last Modified: Mon, 18 Dec 2023 19:51:54 GMT  
		Size: 136.3 MB (136291443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f08613babe22bc1ad31279c88ff461d3fa57f4ca2de2e1d6e6da1131c7221f`  
		Last Modified: Mon, 18 Dec 2023 19:51:50 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:53e4680211790eb8e1101d6dbfcd5e4e9a6563a9f3322cbfb5c7e173b8827355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d6cba73816742bff3c13a0467d1b9241a73771203ac868e601bd03bd12a657`

```dockerfile
```

-	Layers:
	-	`sha256:9c876eabfc58b400fc968bb3a780b22f756b348813c8fad51584d4f12bc99050`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 2.7 MB (2724284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e1c1732aeca2963e5d13eea48fe166ebf71db53b0c57a991ebedd0078f9944`  
		Last Modified: Mon, 18 Dec 2023 19:51:47 GMT  
		Size: 27.9 KB (27897 bytes)  
		MIME: application/vnd.in-toto+json
