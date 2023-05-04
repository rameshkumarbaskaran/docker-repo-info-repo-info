## `mongo:jammy`

```console
$ docker pull mongo@sha256:f9b47ae0144d0f5665c7e716e8c5d745832945a6bd9d15db7ca9128ee09f4fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:9d2f56b066370e614cc6edcd975aba5ac1926c24e63d10bcf8f626bbf75dfdff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236672808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b33e239cde686e9378f9d8941eafa167fdf73527e9e006ab1fe9174c9622797`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:00:25 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 04 May 2023 08:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:00:35 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 May 2023 08:00:35 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 04 May 2023 08:00:42 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 May 2023 08:00:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 May 2023 08:00:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 04 May 2023 08:00:43 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 04 May 2023 08:00:43 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 08:00:44 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 08:00:44 GMT
ENV MONGO_MAJOR=6.0
# Thu, 04 May 2023 08:00:44 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 04 May 2023 08:00:44 GMT
ENV MONGO_VERSION=6.0.5
# Thu, 04 May 2023 08:01:04 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 04 May 2023 08:01:06 GMT
VOLUME [/data/db /data/configdb]
# Thu, 04 May 2023 08:01:06 GMT
ENV HOME=/data/db
# Thu, 04 May 2023 08:01:06 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Thu, 04 May 2023 08:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 May 2023 08:01:06 GMT
EXPOSE 27017
# Thu, 04 May 2023 08:01:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb83bb7be9889457cf3729cf50df2596a4c21e221943325d43e3621afc85296`  
		Last Modified: Thu, 04 May 2023 08:01:33 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95121721c4c526b9ccd2b5630e6b439780c39872431d4a3bedcbc4769350cdc`  
		Last Modified: Thu, 04 May 2023 08:01:34 GMT  
		Size: 5.0 MB (5027884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799041b403cabf54ac974c77fee7211729ec7ddc13fbabe98f93868f43a32fcb`  
		Last Modified: Thu, 04 May 2023 08:01:34 GMT  
		Size: 1.3 MB (1252462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1828e70ef29acb455c8b97fe8b6bc926a79a105e578b55cf78bd979be29535b5`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3781beae9e4d098a887d213f6d3fbb1c9c9648b3516672f63c534a6aa1ea67`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d575316233327cdb50cd97e5b06250f7e5733f3e9aa5a79ba8821492145fd78`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dd404b40f41e6bc62569ea9d496bb5f3021ac0d86c444ff49fafab36c9afba`  
		Last Modified: Thu, 04 May 2023 08:01:55 GMT  
		Size: 200.0 MB (199953553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599c9d5d1bbb0a5e76f45840a9a67ceee86d5eeebceedeb25ca7509983db28`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 5.0 KB (5020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:9f2cc9797ca4b9935c51bee06ed62993e573609f96bc69c61cf11ee027271eb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230233163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7c0d1c6f737a3fc78d8884c0bbf89b5e044be1d9bda9da82550abb6bacd0b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:51:06 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 04 May 2023 03:51:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:51:18 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 May 2023 03:51:18 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 04 May 2023 03:51:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 May 2023 03:51:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 May 2023 03:51:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 04 May 2023 03:51:25 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 04 May 2023 03:51:25 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 03:51:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 03:51:26 GMT
ENV MONGO_MAJOR=6.0
# Thu, 04 May 2023 03:51:26 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 04 May 2023 03:51:26 GMT
ENV MONGO_VERSION=6.0.5
# Thu, 04 May 2023 03:51:44 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 04 May 2023 03:51:47 GMT
VOLUME [/data/db /data/configdb]
# Thu, 04 May 2023 03:51:48 GMT
ENV HOME=/data/db
# Thu, 04 May 2023 03:51:48 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Thu, 04 May 2023 03:51:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 May 2023 03:51:48 GMT
EXPOSE 27017
# Thu, 04 May 2023 03:51:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c1bc6eb929a761d6c8e4e8e9ca2ca6899807a698ab2ce58119de51c77f0c3f`  
		Last Modified: Thu, 04 May 2023 03:52:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5af3169343953ea89194ebd7f6953d78bf81eda11daaa939e57beec9acd2a30`  
		Last Modified: Thu, 04 May 2023 03:52:12 GMT  
		Size: 5.0 MB (4968460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f5afa97a66a32b032396016f112241bcd27938b1504b994944c902286d9571`  
		Last Modified: Thu, 04 May 2023 03:52:11 GMT  
		Size: 1.2 MB (1185066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05f20747b8314c2fa5c58ac2f2afbe9e5d9d099b795355ece221d2f2cfec7b4`  
		Last Modified: Thu, 04 May 2023 03:52:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5a4df6de089141e46014379b79716d1d54b9ce14a15e2a5cf77d65f460012d`  
		Last Modified: Thu, 04 May 2023 03:52:09 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee7bab4fd177aa035083292992f83182e701972b707eec8852b9329657df6b6`  
		Last Modified: Thu, 04 May 2023 03:52:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49156abc6ec258be9c5856adbcf6e62b5620e6e8e158e017f3d815b64cb5a571`  
		Last Modified: Thu, 04 May 2023 03:52:26 GMT  
		Size: 195.7 MB (195681497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddead51c266b363f76dd7fdf1827f687683dfa7765d7b112a5b856da57daf762`  
		Last Modified: Thu, 04 May 2023 03:52:09 GMT  
		Size: 5.0 KB (5021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
