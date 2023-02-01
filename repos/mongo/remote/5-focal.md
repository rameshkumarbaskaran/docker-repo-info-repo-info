## `mongo:5-focal`

```console
$ docker pull mongo@sha256:0385a8151be2a38b954a8c287e820cc4ebd39b394b209eccc3381be5f6911c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:e340d5a498efbc699bf692e19279ba9ad9f80ebb45068f7eade87fc921b78b82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243700075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb61274e3a5905334fa5395be00ed888173f082a2615ee65d292dabe4191056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 26 Jan 2023 13:19:55 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:19:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:19:57 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Thu, 26 Jan 2023 13:19:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:01:40 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 31 Jan 2023 19:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:01:51 GMT
ENV GOSU_VERSION=1.16
# Tue, 31 Jan 2023 19:01:51 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 31 Jan 2023 19:01:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 31 Jan 2023 19:02:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Jan 2023 19:02:38 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 31 Jan 2023 19:02:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 31 Jan 2023 19:02:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 31 Jan 2023 19:02:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 31 Jan 2023 19:02:39 GMT
ENV MONGO_MAJOR=5.0
# Tue, 31 Jan 2023 19:02:39 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 31 Jan 2023 19:02:39 GMT
ENV MONGO_VERSION=5.0.14
# Tue, 31 Jan 2023 19:03:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 31 Jan 2023 19:03:03 GMT
VOLUME [/data/db /data/configdb]
# Tue, 31 Jan 2023 19:03:03 GMT
ENV HOME=/data/db
# Tue, 31 Jan 2023 19:03:04 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Tue, 31 Jan 2023 19:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Jan 2023 19:03:04 GMT
EXPOSE 27017
# Tue, 31 Jan 2023 19:03:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbded1210cdd8a46fe059c3ce71f66aba02d844f9873fb9163f194353048de4`  
		Last Modified: Tue, 31 Jan 2023 19:05:59 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98cee93150e588d145b9b599da8f25cc21f17d175bbd65351ef17752bb88e2`  
		Last Modified: Tue, 31 Jan 2023 19:06:00 GMT  
		Size: 8.3 MB (8348550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f7eb87ea6d736e92ee550723d159333581fcee4d1c550c4b4e4135dacdc670`  
		Last Modified: Tue, 31 Jan 2023 19:05:59 GMT  
		Size: 1.3 MB (1255800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cdd20e07a50f36bf63e2740942264d8fb11f1842f048c207e3bab339ced7d0`  
		Last Modified: Tue, 31 Jan 2023 19:05:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8559b256835fe8f92032b9c77811151f505820f72dc9b92f0673f9fe8453d0a`  
		Last Modified: Tue, 31 Jan 2023 19:06:36 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494bdae77931c8c1df8dafe3cced0892d087015caf225269e308e8ee8cad5da8`  
		Last Modified: Tue, 31 Jan 2023 19:06:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4998963b3e2df4fe60c0d4c31ae3f8d477b6bde467d78cee21fc95d7cf53009d`  
		Last Modified: Tue, 31 Jan 2023 19:07:02 GMT  
		Size: 205.5 MB (205509201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080ea8bed1afea25d18498cabb4ddbae2df89fa1a87faa87df1fe40607ee6368`  
		Last Modified: Tue, 31 Jan 2023 19:06:36 GMT  
		Size: 5.0 KB (4957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:595c9cfeb19df46ff88f7ea7f3fd31a968ef6376d7c851fe2bd4b14a121066b3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236227016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e7c3fa4e31f4a80f64226579d6abe7548913e8d9b3255c3dd58a4a8c6909e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:03:40 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 01 Feb 2023 19:03:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:03:55 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 19:03:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 01 Feb 2023 19:04:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 19:04:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 01 Feb 2023 19:04:38 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 19:04:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 01 Feb 2023 19:04:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 01 Feb 2023 19:04:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 01 Feb 2023 19:04:38 GMT
ENV MONGO_MAJOR=5.0
# Wed, 01 Feb 2023 19:04:39 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 01 Feb 2023 19:04:39 GMT
ENV MONGO_VERSION=5.0.14
# Wed, 01 Feb 2023 19:04:57 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 01 Feb 2023 19:05:01 GMT
VOLUME [/data/db /data/configdb]
# Wed, 01 Feb 2023 19:05:01 GMT
ENV HOME=/data/db
# Wed, 01 Feb 2023 19:05:01 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Wed, 01 Feb 2023 19:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 19:05:01 GMT
EXPOSE 27017
# Wed, 01 Feb 2023 19:05:01 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197e79a593996392dc9c7dea7b4eebe9567f190b13e33b96315e3fa7bfe0cbff`  
		Last Modified: Wed, 01 Feb 2023 19:06:35 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a54d19161368d031ebb2bd8697e5077e32faea13ed42ef3bc01f1521db0b059`  
		Last Modified: Wed, 01 Feb 2023 19:06:36 GMT  
		Size: 8.2 MB (8177815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8547f0e899b28966b8bd3a9247256403aacd1bfe5043f9848fabacbfb38ffd92`  
		Last Modified: Wed, 01 Feb 2023 19:06:35 GMT  
		Size: 1.2 MB (1188343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315a8963db2b1f685b9da4bc23fab83cc03ce32eff34be384499607a1416459e`  
		Last Modified: Wed, 01 Feb 2023 19:06:29 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b8bff0c93bb6c7656d92339cae1e49d941df6d7f9c22f059c33df4e52478ca`  
		Last Modified: Wed, 01 Feb 2023 19:07:00 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d90acd9b0e57e90217a0b2bb6ae09053cb65cb487bba729ef69a1ac2b68f27`  
		Last Modified: Wed, 01 Feb 2023 19:07:00 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aebc006dc107ed8b5e0e87aef3f634a3ac64d89dcb55ea6cb008f554a53ebf`  
		Last Modified: Wed, 01 Feb 2023 19:07:20 GMT  
		Size: 199.7 MB (199658472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e43614101f4fc8e21d44db66e61473e1c760f657e9810762bfe9d866b678b85`  
		Last Modified: Wed, 01 Feb 2023 19:07:00 GMT  
		Size: 5.0 KB (4962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
