## `mongo:4-focal`

```console
$ docker pull mongo@sha256:db6dd8229c81cf06be5108fc595dfc2ae2e282b057559cb94d548182843b7911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:40d8a1af82bcc8472cf251c7c47e7b217379801704f99c6c6dac3a30e036f4d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175860469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcde8b068debffbb7516787f13d7b0e4e2cb38cac275dc70bb3d3247faa1446`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 02:43:43 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 03 May 2023 04:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 04:29:00 GMT
ENV GOSU_VERSION=1.16
# Wed, 03 May 2023 04:29:00 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 03 May 2023 04:29:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 03 May 2023 04:29:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 03 May 2023 04:29:52 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 03 May 2023 04:29:53 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 03 May 2023 04:29:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 03 May 2023 04:29:53 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 03 May 2023 04:29:53 GMT
ENV MONGO_MAJOR=4.4
# Wed, 03 May 2023 04:29:53 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 03 May 2023 04:29:53 GMT
ENV MONGO_VERSION=4.4.21
# Wed, 03 May 2023 04:30:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 03 May 2023 04:30:15 GMT
VOLUME [/data/db /data/configdb]
# Wed, 03 May 2023 04:30:15 GMT
ENV HOME=/data/db
# Wed, 03 May 2023 04:30:15 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Wed, 03 May 2023 04:30:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 May 2023 04:30:15 GMT
EXPOSE 27017
# Wed, 03 May 2023 04:30:15 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6653ceb2297789e4fe13aba3af53f096e83ecc4ad4417356ea72e4f9e8b7dccb`  
		Last Modified: Tue, 18 Apr 2023 02:45:51 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e067c5774dde349c4127278bc0f06acc2f6d6a88bff74983171225648b999315`  
		Last Modified: Wed, 03 May 2023 04:32:35 GMT  
		Size: 8.3 MB (8348562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2512535c9bcf2f6101b06b4fe0ed1c287f5468ff706040b190898672771028`  
		Last Modified: Wed, 03 May 2023 04:32:34 GMT  
		Size: 1.3 MB (1255808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95823dd641199b73cc53f548fee010eee561dfe2ebae9a7ee571fe1452e33db0`  
		Last Modified: Wed, 03 May 2023 04:32:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77aa83f4fcd45980c2c2021d468afcafa5304e8eb8c52ee764a7fdde6cd9114f`  
		Last Modified: Wed, 03 May 2023 04:33:07 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db43fff6317e9a52a188953f49dfb64fab77e277338c7c6e5a93e6121cc600d`  
		Last Modified: Wed, 03 May 2023 04:33:07 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abb8f5c5e6670f7aa6bcc5fe9d0dfc782d714e07edb9842a525739ac12e9be2`  
		Last Modified: Wed, 03 May 2023 04:33:22 GMT  
		Size: 137.7 MB (137668827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccc4657b334384e0d325da53ba88aca4ad6bb224d8b2352f821e4223944f20c`  
		Last Modified: Wed, 03 May 2023 04:33:07 GMT  
		Size: 5.0 KB (5019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ce5cd79118be21ef36bd53ce30501ca708ef89ac5c37b5e40d5d3a2ad85db644
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171495189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0fe5dbdf82021e4605aee4223ecb79dea4557dbd81439f3db203c39ab106e3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:57:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 03 May 2023 03:47:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:47:47 GMT
ENV GOSU_VERSION=1.16
# Wed, 03 May 2023 03:47:47 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 03 May 2023 03:47:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 03 May 2023 03:47:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 03 May 2023 03:48:38 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 03 May 2023 03:48:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 03 May 2023 03:48:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 03 May 2023 03:48:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 03 May 2023 03:48:39 GMT
ENV MONGO_MAJOR=4.4
# Wed, 03 May 2023 03:48:39 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 24 May 2023 00:45:49 GMT
ENV MONGO_VERSION=4.4.22
# Wed, 24 May 2023 00:46:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 24 May 2023 00:46:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 24 May 2023 00:46:04 GMT
ENV HOME=/data/db
# Wed, 24 May 2023 00:46:04 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Wed, 24 May 2023 00:46:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 00:46:04 GMT
EXPOSE 27017
# Wed, 24 May 2023 00:46:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c7ba53fe6d965200e96c72021fd3bee66138e7ae32fda40347d832ca07c4c`  
		Last Modified: Tue, 18 Apr 2023 01:59:09 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98de930ed0eb92a28b1702a22726d9e7e758797d1d25717a0cd817996e0dd58`  
		Last Modified: Wed, 03 May 2023 03:51:06 GMT  
		Size: 8.2 MB (8179716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3506d1a4618d9841c72c1c1cdcd5ee3a21454c69647995922f810059f9800d8d`  
		Last Modified: Wed, 03 May 2023 03:51:06 GMT  
		Size: 1.2 MB (1188964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471e077bfc9d9ff7b181540272893c7b7d31af0bc48f43d2b627ed965070a67`  
		Last Modified: Wed, 03 May 2023 03:51:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36610876a6054fac94ff3a7faf8882165f8d0091212b78c88dec635fcf7fbd6`  
		Last Modified: Wed, 03 May 2023 03:51:32 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af06266c0e5928eb6e7b3f36a6be919ffdab4567158ea9c7f7f7289d0d21d35`  
		Last Modified: Wed, 03 May 2023 03:51:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bab028fc827da01808feb7cfc55bd2fb5aaf3933d11f4818404d7a8e4778a`  
		Last Modified: Wed, 24 May 2023 00:47:35 GMT  
		Size: 134.9 MB (134921401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3072c3bddcf5f6fd025978e0b5d1da2eace13f7d41b6f35f63eae8ed51d85288`  
		Last Modified: Wed, 24 May 2023 00:47:24 GMT  
		Size: 5.0 KB (5020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
