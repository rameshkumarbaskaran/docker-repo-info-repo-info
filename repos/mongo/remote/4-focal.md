## `mongo:4-focal`

```console
$ docker pull mongo@sha256:a16296827fe26e28d773ce18b99d2d04e02640845e441bbe85de44b19a9f13bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:a88d9e1d0bbf6fd4b57f4accc9000b0f3a76b2d9216180788d92956a7437ea0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172837363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba92ac6108e65933b60e1bd9d03bd8713502d39af6096551c16fe145ca1f807`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:30:12 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 05 Oct 2022 18:30:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:30:20 GMT
ENV GOSU_VERSION=1.12
# Wed, 05 Oct 2022 18:30:20 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 05 Oct 2022 18:30:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 18:30:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 18:31:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 05 Oct 2022 18:31:44 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 05 Oct 2022 18:31:44 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 18:31:44 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 18:31:44 GMT
ENV MONGO_MAJOR=4.4
# Wed, 05 Oct 2022 18:31:45 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 05 Oct 2022 18:31:45 GMT
ENV MONGO_VERSION=4.4.17
# Wed, 05 Oct 2022 18:32:03 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 05 Oct 2022 18:32:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 05 Oct 2022 18:32:04 GMT
ENV HOME=/data/db
# Wed, 05 Oct 2022 18:32:05 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Wed, 05 Oct 2022 18:32:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:32:05 GMT
EXPOSE 27017
# Wed, 05 Oct 2022 18:32:05 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81bcd64a2d26fbd2741700cc3f6f1aa783ae202298d8010aca8c60f034c4e59`  
		Last Modified: Wed, 05 Oct 2022 18:33:32 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ed91f63dfa037fa6061dee8f91d31f24a66375c70d652e8ee3c77e9e20b0fe`  
		Last Modified: Wed, 05 Oct 2022 18:33:33 GMT  
		Size: 3.1 MB (3059535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d1770a2c11d56f4506d0efdc18d345c397565f38270c9f33347a483a8bfb58`  
		Last Modified: Wed, 05 Oct 2022 18:33:33 GMT  
		Size: 6.5 MB (6505968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d917eab2f0dc57fe40f116099f93a233b75e63df943d2a84d37623faf91ed`  
		Last Modified: Wed, 05 Oct 2022 18:33:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae23fd926d5289d7f9939344270c99e24906888a69783c1d69bfd2cd5d522d60`  
		Last Modified: Wed, 05 Oct 2022 18:34:54 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e23a31f26283ab44fab40c519e3cdf154a2b4f38cd7b70a0cd5772124f39240`  
		Last Modified: Wed, 05 Oct 2022 18:34:54 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1670c0330a4ef40749c20aa01f2a34e2b097b637f93d81f30572450696cb32`  
		Last Modified: Wed, 05 Oct 2022 18:35:12 GMT  
		Size: 134.7 MB (134688648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e00f823fe51d15240f771d361ef692401c41aa1a69881afbcb4bfe81cf8fa6`  
		Last Modified: Wed, 05 Oct 2022 18:34:54 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:1f48bd9ab60c129ae2ead986a360c615b6f5b1b82e0897f23c5659d1902f5e26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167669316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da175e22741619b68f31e9e67d552e0ad47ecc98def5e042ea8be7bdf03b021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:54:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 05 Oct 2022 16:54:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 16:54:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 05 Oct 2022 16:54:46 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 05 Oct 2022 16:55:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 16:55:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 16:56:32 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 05 Oct 2022 16:56:32 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 05 Oct 2022 16:56:33 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 16:56:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 16:56:35 GMT
ENV MONGO_MAJOR=4.4
# Wed, 05 Oct 2022 16:56:36 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 05 Oct 2022 16:56:37 GMT
ENV MONGO_VERSION=4.4.17
# Wed, 05 Oct 2022 16:56:54 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 05 Oct 2022 16:56:54 GMT
VOLUME [/data/db /data/configdb]
# Wed, 05 Oct 2022 16:56:55 GMT
ENV HOME=/data/db
# Wed, 05 Oct 2022 16:56:57 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Wed, 05 Oct 2022 16:56:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:56:58 GMT
EXPOSE 27017
# Wed, 05 Oct 2022 16:56:59 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808a7df5fbbc12c4cd8f740fabdbbe301d6a4efe1b81b3f196474a28d0322c92`  
		Last Modified: Wed, 05 Oct 2022 16:59:14 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5a5e151a7f04dcea23cd214c84a62e5c02bfd8bf21e50b6384cb32a7dac4ed`  
		Last Modified: Wed, 05 Oct 2022 16:59:14 GMT  
		Size: 2.9 MB (2905895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbed2c86a740691aafa2028087ed2a11f64352f3ab06a520efa22bc7c5246f03`  
		Last Modified: Wed, 05 Oct 2022 16:59:14 GMT  
		Size: 6.2 MB (6248099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c6dc442fc2aca80b585c0c229cf8addb668c43cb2b7b15193532981186e6d`  
		Last Modified: Wed, 05 Oct 2022 16:59:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d58eccfdc8f9092600d4b81f9b97a07e2593961ac2d47eaaec816461ab67150`  
		Last Modified: Wed, 05 Oct 2022 17:00:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31ac6ce89932dbf353f6a8e8486f84631f8a0246d9399e0eab4f7f9f36bbee`  
		Last Modified: Wed, 05 Oct 2022 17:00:38 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ee9553fd5f3d5eb07720864b5545c94ddca7d377be05c309c4d92e0628a622`  
		Last Modified: Wed, 05 Oct 2022 17:00:54 GMT  
		Size: 131.3 MB (131315081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4dbde1ca5831c155bcb135e515c63e9aa352cb0a926cc4cea9978ad0ae0d11`  
		Last Modified: Wed, 05 Oct 2022 17:00:38 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
