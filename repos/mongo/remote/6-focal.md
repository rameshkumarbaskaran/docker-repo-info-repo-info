## `mongo:6-focal`

```console
$ docker pull mongo@sha256:f2beede7890ec15c7ea8b8d38007c3be1be0c4fb8c27bd2d40b4d437b63f44f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:6-focal` - linux; amd64

```console
$ docker pull mongo@sha256:3fa5e59fdb0b7c42bd2db52142ecbc673b0c1356b115b9ad2b32436e14281e4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232074458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd27bb6d3e6ef0dc97e0ea1e29ec2213e6c384ff69340f553d08a4f76cc0623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:37:18 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 25 Oct 2022 17:37:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 17:37:28 GMT
ENV GOSU_VERSION=1.12
# Tue, 25 Oct 2022 17:37:28 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 25 Oct 2022 17:37:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 17:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 17:37:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 25 Oct 2022 17:37:45 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 25 Oct 2022 17:37:45 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 25 Oct 2022 17:37:45 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 25 Oct 2022 17:37:45 GMT
ENV MONGO_MAJOR=6.0
# Tue, 25 Oct 2022 17:37:46 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 16 Nov 2022 19:36:44 GMT
ENV MONGO_VERSION=6.0.3
# Wed, 16 Nov 2022 19:37:17 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 16 Nov 2022 19:37:19 GMT
VOLUME [/data/db /data/configdb]
# Wed, 16 Nov 2022 19:37:19 GMT
ENV HOME=/data/db
# Wed, 16 Nov 2022 19:37:19 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Wed, 16 Nov 2022 19:37:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Nov 2022 19:37:19 GMT
EXPOSE 27017
# Wed, 16 Nov 2022 19:37:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a00eb9f68a0dcf2f4b6f3881376f35b2908e0ec03e0ba7b41dce5138a57017e`  
		Last Modified: Wed, 26 Oct 2022 16:14:33 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f683956749c518e0ea925e30c0c5115c4ce12e827cd34bcf72ce2e9d750a2bb6`  
		Last Modified: Wed, 26 Oct 2022 16:14:35 GMT  
		Size: 3.1 MB (3059607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b2f05ea206b8ad00c6db544ddc80db3b9f6f9ea070867894eb83acdd9656c`  
		Last Modified: Tue, 25 Oct 2022 17:40:52 GMT  
		Size: 6.5 MB (6509130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a342bea915a9cfedf83084c321b2c1aae8bbfdc8aa1f0845669c4d325bff96d`  
		Last Modified: Tue, 25 Oct 2022 17:40:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa956ab1c2f09b41dec38b203cd914272b87e515a3658915e57f3a686382c261`  
		Last Modified: Tue, 25 Oct 2022 17:40:30 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a8542a62498c9e71e1778b9b0bfbf522b4e549b83a9b4f64f7c1b671ae7df`  
		Last Modified: Tue, 25 Oct 2022 17:40:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5a5d2ec8221695c3de17dafdadeb54a979f8adf5d1225e77ef9a4957897ed4`  
		Last Modified: Wed, 16 Nov 2022 19:38:48 GMT  
		Size: 193.9 MB (193919125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37200fef7cf6cc4504e04a4be54d1618e914b80ee98f0a9514f3b286ce434b32`  
		Last Modified: Wed, 16 Nov 2022 19:38:21 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d8533eaab21bb20cbe92deff4ac189970002d65a69a0ea09efd50c14123acb80
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225418773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a36871c855789d864a73a6623f7d680a889828dccf3d4f4af7706c0d60dcc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:12:08 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 26 Oct 2022 02:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:12:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 26 Oct 2022 02:12:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 26 Oct 2022 02:12:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:12:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:12:28 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 26 Oct 2022 02:12:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 26 Oct 2022 02:12:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 26 Oct 2022 02:12:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 26 Oct 2022 02:12:28 GMT
ENV MONGO_MAJOR=6.0
# Wed, 26 Oct 2022 02:12:28 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 16 Nov 2022 20:07:30 GMT
ENV MONGO_VERSION=6.0.3
# Wed, 16 Nov 2022 20:08:08 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 16 Nov 2022 20:08:12 GMT
VOLUME [/data/db /data/configdb]
# Wed, 16 Nov 2022 20:08:12 GMT
ENV HOME=/data/db
# Wed, 16 Nov 2022 20:08:12 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Wed, 16 Nov 2022 20:08:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Nov 2022 20:08:12 GMT
EXPOSE 27017
# Wed, 16 Nov 2022 20:08:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffac05d305dafc7bd6d968c4d611342ceb95a87494c361ab37718b188f02763`  
		Last Modified: Wed, 26 Oct 2022 02:16:20 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d44feb31079d0e2421a83a8dd5563d203ec1ff537396d3ed65dd35cdfed206f`  
		Last Modified: Wed, 26 Oct 2022 02:16:21 GMT  
		Size: 2.9 MB (2907461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd79df0bf56efa1ec22177052bd5d6e4feef423ad95176bd0f86a478f3f99d30`  
		Last Modified: Wed, 26 Oct 2022 02:16:21 GMT  
		Size: 6.4 MB (6425791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393c4defd29fb265c4d4794d5f008fbde7c8d9c4f91a7105e9cf2866a28df77a`  
		Last Modified: Wed, 26 Oct 2022 02:16:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2da71c1f524304c6fddcfd682ea28128baf5f08cadfbf5b9c0ad090af3831d`  
		Last Modified: Wed, 26 Oct 2022 02:16:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4c4322236bd8250387800e057c330d487ebf386f2d007d7ccb8bc9aabc13e1`  
		Last Modified: Wed, 26 Oct 2022 02:16:18 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587da6358a4fb65b90e0b938996b8e842c3804b1713be364360d8675803e5412`  
		Last Modified: Wed, 16 Nov 2022 20:09:29 GMT  
		Size: 188.9 MB (188880764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0236cbe0a30bbad69de948cad326331858d4138efbdd029cd03143bf50d92d`  
		Last Modified: Wed, 16 Nov 2022 20:09:10 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
