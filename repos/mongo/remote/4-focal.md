## `mongo:4-focal`

```console
$ docker pull mongo@sha256:1aa63c78bd174e5c4c6dbdbf0ad22ba6daaa0a0e44f9ff50b7b2c613d9bba862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:9909a039a7d237d081bb208ce7eb7c9824dd091f8e277d4b32a8de188c3c53c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176053986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b0e0662b9a8a4413901fdaf4144b63a8daf3dd1ee72a47e1cedb97a73eb28c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:37:40 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 04 Jul 2023 18:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:37:54 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 18:37:54 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 04 Jul 2023 18:38:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 18:38:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 18:39:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 18:39:37 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 04 Jul 2023 18:39:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 04 Jul 2023 18:39:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 04 Jul 2023 18:39:38 GMT
ENV MONGO_MAJOR=4.4
# Tue, 04 Jul 2023 18:39:38 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 14 Jul 2023 00:21:37 GMT
ENV MONGO_VERSION=4.4.23
# Fri, 14 Jul 2023 00:21:55 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 14 Jul 2023 00:21:56 GMT
VOLUME [/data/db /data/configdb]
# Fri, 14 Jul 2023 00:21:56 GMT
ENV HOME=/data/db
# Fri, 14 Jul 2023 00:21:56 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Fri, 14 Jul 2023 00:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jul 2023 00:21:56 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 00:21:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb7d9e7beb16f8524b1364b05291e986d13fe9e41a3527c0df712b6488ccd5`  
		Last Modified: Tue, 04 Jul 2023 18:42:08 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8673b711682ec60ce786477043890cd2390b807b1ba6626eb5d11679187fa60`  
		Last Modified: Tue, 04 Jul 2023 18:42:09 GMT  
		Size: 8.4 MB (8374126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38f30c6ed576db67667e1e67bc05ec390f5bae0168fa33f40146fc13227c529`  
		Last Modified: Tue, 04 Jul 2023 18:42:08 GMT  
		Size: 1.3 MB (1256098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d115e2a9dcf0698551b83906207c5d79faa89c5a947f926bfe11cb95a4726b7`  
		Last Modified: Tue, 04 Jul 2023 18:42:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1908425bccb8c42abbd85af80e827c1bdd237508d4a179f7ce424743235f8ddc`  
		Last Modified: Tue, 04 Jul 2023 18:43:40 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc65cb70f9c5d23019a1ec2ebd4ac46858b127da4b9618f441ed0adcd47f6344`  
		Last Modified: Tue, 04 Jul 2023 18:43:40 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a284ad28140b7fc00027cb2d74d0bdaf3ffae73c0e3b4ec8803561bf503c9a4`  
		Last Modified: Fri, 14 Jul 2023 00:24:26 GMT  
		Size: 137.8 MB (137835065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0131638481b2b49b1847ea920767cead4bd43299a7ba9bd1fbb118ffc681b861`  
		Last Modified: Fri, 14 Jul 2023 00:24:10 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:aa495491a5e79271ec5688ebb2cdeaf037747721c71709c8581360d249e1ea54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171683271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42daf74f66b04140e68045d9339a25fb07d6734229944b1596ea6cefb8115b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 14:08:58 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 04 Jul 2023 14:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:09:44 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 14:09:44 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 04 Jul 2023 14:09:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 14:09:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 14:11:24 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 14:11:24 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 04 Jul 2023 14:11:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 04 Jul 2023 14:11:24 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 04 Jul 2023 14:11:24 GMT
ENV MONGO_MAJOR=4.4
# Tue, 04 Jul 2023 14:11:24 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 14 Jul 2023 00:41:29 GMT
ENV MONGO_VERSION=4.4.23
# Fri, 14 Jul 2023 00:41:42 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 14 Jul 2023 00:41:44 GMT
VOLUME [/data/db /data/configdb]
# Fri, 14 Jul 2023 00:41:44 GMT
ENV HOME=/data/db
# Fri, 14 Jul 2023 00:41:44 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Fri, 14 Jul 2023 00:41:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jul 2023 00:41:45 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 00:41:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25b95aa00873e82f18551cf2442a5aa67c3da3b3bbb3f23b5649603bdee16e3`  
		Last Modified: Tue, 04 Jul 2023 14:13:32 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128f03cad838ed6cc4fb08e5b9110b64cd0cfacbca6a72ce6b4ae92bf74620e9`  
		Last Modified: Tue, 04 Jul 2023 14:13:33 GMT  
		Size: 8.2 MB (8202326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4514438b12b86968e33c10d7fc1b604d90f3b02863b6d84f5454274e954ca414`  
		Last Modified: Tue, 04 Jul 2023 14:13:32 GMT  
		Size: 1.2 MB (1189106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64c12ed4a7fa6ce85cbc271ea8d1a0854eca21467950aec1a441d278bf84664`  
		Last Modified: Tue, 04 Jul 2023 14:13:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3846ec4993eabed027f51a532ff8a3b40e4fa3a1086c77b04a74af32c98e66`  
		Last Modified: Tue, 04 Jul 2023 14:14:46 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2b6ad529076f8dd575a32ce077d4712ab6477ac5ad662b675003ae7327333d`  
		Last Modified: Tue, 04 Jul 2023 14:14:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126d2b20bee1130a65d0e69c5d53a6c024e2f9b92b68b98a5c93c5f1041f60c9`  
		Last Modified: Fri, 14 Jul 2023 00:43:46 GMT  
		Size: 135.1 MB (135084814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec23fd63f8d822b9347e9b46d91e90f9b1f8d1faac9a99a12fde95fc620a248d`  
		Last Modified: Fri, 14 Jul 2023 00:43:35 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
