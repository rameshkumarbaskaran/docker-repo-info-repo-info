## `mongo:4-focal`

```console
$ docker pull mongo@sha256:5e1edb7fc72f9f5ae1f777ef0dace8ed248837e5c036841f43bb2fee4aba8648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:422a3a380688eca8ed45b7952f64d04de20f54f2e3616a4c35aeebbf8d241252
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173151913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcde7fa7593b5be4dc271aff2b837bb80039cf10b29e6c26fde2e0729f58327`
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
# Tue, 31 Jan 2023 19:03:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 31 Jan 2023 19:03:41 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 31 Jan 2023 19:03:41 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 31 Jan 2023 19:03:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 31 Jan 2023 19:03:41 GMT
ENV MONGO_MAJOR=4.4
# Tue, 31 Jan 2023 19:03:42 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 31 Jan 2023 19:03:42 GMT
ENV MONGO_VERSION=4.4.18
# Tue, 31 Jan 2023 19:03:59 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 31 Jan 2023 19:03:59 GMT
VOLUME [/data/db /data/configdb]
# Tue, 31 Jan 2023 19:04:00 GMT
ENV HOME=/data/db
# Tue, 31 Jan 2023 19:04:00 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Tue, 31 Jan 2023 19:04:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Jan 2023 19:04:00 GMT
EXPOSE 27017
# Tue, 31 Jan 2023 19:04:00 GMT
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
	-	`sha256:e4055bdfc50ec98e0fdb76ad0289b16d15648cdf125d89a40bfafdf6a0d74d97`  
		Last Modified: Tue, 31 Jan 2023 19:07:39 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8194a0b81f6b7f2ba131712353561a2645ce893e29eca98d6140d99ced4561`  
		Last Modified: Tue, 31 Jan 2023 19:07:39 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca83528f7f070d0b5cb6a0bb590eaa80908db19a3a03d0c0411d63f2a0380ca`  
		Last Modified: Tue, 31 Jan 2023 19:07:57 GMT  
		Size: 135.0 MB (134961038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00108ee323452b3ce483f6dc4e7001b2274c6e81d80dfc6ea314504d5c80a34`  
		Last Modified: Tue, 31 Jan 2023 19:07:39 GMT  
		Size: 5.0 KB (4960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4921da2988df3e8b1ebd262f251dc743db0f9ac087f80ea8dde174404171f7ff
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168092319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3d163ac58fe483d17382884c38ff23db0290443b5366e1bc24b1b6a240fce9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:02:15 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 31 Jan 2023 18:02:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:02:30 GMT
ENV GOSU_VERSION=1.12
# Tue, 31 Jan 2023 18:02:30 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 31 Jan 2023 18:02:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 31 Jan 2023 18:02:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Jan 2023 18:04:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 31 Jan 2023 18:04:09 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 31 Jan 2023 18:04:09 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 31 Jan 2023 18:04:09 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 31 Jan 2023 18:04:09 GMT
ENV MONGO_MAJOR=4.4
# Tue, 31 Jan 2023 18:04:10 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 31 Jan 2023 18:04:10 GMT
ENV MONGO_VERSION=4.4.18
# Tue, 31 Jan 2023 18:04:25 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 31 Jan 2023 18:04:27 GMT
VOLUME [/data/db /data/configdb]
# Tue, 31 Jan 2023 18:04:27 GMT
ENV HOME=/data/db
# Tue, 31 Jan 2023 18:04:27 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Tue, 31 Jan 2023 18:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Jan 2023 18:04:28 GMT
EXPOSE 27017
# Tue, 31 Jan 2023 18:04:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb0be2197a935d43d4bb8912a5ae267e601c98d6e380aa6c20d5bb729e5d01d`  
		Last Modified: Tue, 31 Jan 2023 18:06:00 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ab27065f63560cee0ad6f472acf7517eb482e82fb5c3aa4729ab5c40f7861e`  
		Last Modified: Tue, 31 Jan 2023 18:06:01 GMT  
		Size: 8.2 MB (8177787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a43a7130289bf7a7dd9379e9e3f1dbfe9f4d73583878b9959d13da08b42eeb`  
		Last Modified: Tue, 31 Jan 2023 18:06:00 GMT  
		Size: 1.2 MB (1170798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c239b62d08c80a0eb95fb730156af25ff21f50d9c55e8100c584c3bbf02e4a5`  
		Last Modified: Tue, 31 Jan 2023 18:05:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42099ad7bd22c12c771bd5e8b9c8b7eb5e6352bcd0e027781740c3fade69728e`  
		Last Modified: Tue, 31 Jan 2023 18:07:21 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e49518a9a06728d13134a864fb08f45f376e254b8c516f5b02abbde04708f5`  
		Last Modified: Tue, 31 Jan 2023 18:07:21 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638ea5500d20ce8089e4b51744f4e2bcb4beabd3a7fcc32a1e1552ad3d7b28c3`  
		Last Modified: Tue, 31 Jan 2023 18:07:34 GMT  
		Size: 131.5 MB (131541346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c43fe3d68828681a60b53aaf5cb73a488b76fcfcc220a10fe16008010362c0`  
		Last Modified: Tue, 31 Jan 2023 18:07:21 GMT  
		Size: 5.0 KB (4962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
