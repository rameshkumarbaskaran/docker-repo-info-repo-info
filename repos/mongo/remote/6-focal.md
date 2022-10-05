## `mongo:6-focal`

```console
$ docker pull mongo@sha256:649755633610633762b119385c1f4294c7593aaeba7f6477d438955d0c91af24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:6-focal` - linux; amd64

```console
$ docker pull mongo@sha256:e0b1614551474ee2f3c3ef7c9706b5e19f2107aa36b73c910522af9fa8eb756e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231723662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cca5cf682396e2ad3b4af822f1e0f64990a940cf9047c8d93b63af592e054aa`
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
# Wed, 05 Oct 2022 18:30:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 05 Oct 2022 18:30:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 05 Oct 2022 18:30:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 18:30:35 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 18:30:35 GMT
ENV MONGO_MAJOR=6.0
# Wed, 05 Oct 2022 18:30:35 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 05 Oct 2022 18:30:35 GMT
ENV MONGO_VERSION=6.0.2
# Wed, 05 Oct 2022 18:30:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 05 Oct 2022 18:30:59 GMT
VOLUME [/data/db /data/configdb]
# Wed, 05 Oct 2022 18:30:59 GMT
ENV HOME=/data/db
# Wed, 05 Oct 2022 18:30:59 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Wed, 05 Oct 2022 18:31:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:31:00 GMT
EXPOSE 27017
# Wed, 05 Oct 2022 18:31:00 GMT
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
	-	`sha256:d0226311fde3e7d308a8f05fcaae80f725c42a8094ac2b43ec3f2f620a56900d`  
		Last Modified: Wed, 05 Oct 2022 18:33:30 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf22b9bccca1cc8038cc7e33eadd8e43b69b9cd44f141529029365fdf0308dd2`  
		Last Modified: Wed, 05 Oct 2022 18:33:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4955b612fd63dc899305e7e50aff0bf7ab5e6dfedb95a184857d50e044c669`  
		Last Modified: Wed, 05 Oct 2022 18:33:57 GMT  
		Size: 193.6 MB (193574947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8341d9c8d5bd44deb9b5a949893e592e59b66a4de7d056f86568f05f53c7a6`  
		Last Modified: Wed, 05 Oct 2022 18:33:30 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0a6f2b19ee2f8c5193fa286524aa9949c3a68af5b2e8440d2f593996376504c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224938630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa885bebec49cae70e782b1d0fcb92fccebfb386ccd76251ceb1b0f99e08bb04`
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
# Wed, 05 Oct 2022 16:55:05 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 05 Oct 2022 16:55:06 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 05 Oct 2022 16:55:07 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 16:55:08 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 16:55:09 GMT
ENV MONGO_MAJOR=6.0
# Wed, 05 Oct 2022 16:55:10 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 05 Oct 2022 16:55:11 GMT
ENV MONGO_VERSION=6.0.2
# Wed, 05 Oct 2022 16:55:34 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 05 Oct 2022 16:55:35 GMT
VOLUME [/data/db /data/configdb]
# Wed, 05 Oct 2022 16:55:35 GMT
ENV HOME=/data/db
# Wed, 05 Oct 2022 16:55:37 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Wed, 05 Oct 2022 16:55:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:55:38 GMT
EXPOSE 27017
# Wed, 05 Oct 2022 16:55:39 GMT
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
	-	`sha256:70d00e8640a3f0c64b7cd189730daacde9c594bf5850cda768e9e0f97bfbfbcc`  
		Last Modified: Wed, 05 Oct 2022 16:59:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11bc600eb8d283a1a0030c98e1856fd8b96b8f8c86fd7feb0cf74e710e168b4`  
		Last Modified: Wed, 05 Oct 2022 16:59:11 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b720c57555ba599236671087a8d9d0dae2da8d3677a9e9c240128242c28796`  
		Last Modified: Wed, 05 Oct 2022 16:59:37 GMT  
		Size: 188.6 MB (188584399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194b45d19c19e2b2b24ad7d9b21b2be0ad2e16c100733b8f0ce8ed73fae5873e`  
		Last Modified: Wed, 05 Oct 2022 16:59:11 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
