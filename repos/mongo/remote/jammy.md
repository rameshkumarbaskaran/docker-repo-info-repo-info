## `mongo:jammy`

```console
$ docker pull mongo@sha256:d9b7d9ae0143c366c49efdfbae23dd54ca4d921b7abb985788427f5c482a9e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:05bb0d03427adc9f27eb93b02dd501e4f852f3ff46144bfd42a227721c496e1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258557681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be86e9501b0e50de30296bf6f92d0126fa2c0bf144aa833caa5d4cc66c840aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:54:06 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Oct 2023 06:54:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:54:21 GMT
ENV GOSU_VERSION=1.16
# Tue, 03 Oct 2023 06:54:21 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 03 Oct 2023 06:54:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 03 Oct 2023 06:54:29 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 03 Oct 2023 06:54:30 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 03 Oct 2023 06:54:30 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 03 Oct 2023 06:54:30 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 03 Oct 2023 06:54:30 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 03 Oct 2023 06:54:30 GMT
ENV MONGO_MAJOR=7.0
# Tue, 03 Oct 2023 06:54:31 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Oct 2023 06:54:31 GMT
ENV MONGO_VERSION=7.0.2
# Tue, 03 Oct 2023 06:54:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Oct 2023 06:54:55 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Oct 2023 06:54:55 GMT
ENV HOME=/data/db
# Tue, 03 Oct 2023 06:54:55 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Tue, 03 Oct 2023 06:54:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2023 06:54:55 GMT
EXPOSE 27017
# Tue, 03 Oct 2023 06:54:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ac84d07e956a21a84edd5656ca5f8c6a4d46b774a69a9c6bb1307ea3c07a59`  
		Last Modified: Tue, 03 Oct 2023 06:55:58 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce678af55db40aca17e12e2491540b0db04997abe68d23bee7ee26bc679cab62`  
		Last Modified: Tue, 03 Oct 2023 06:55:59 GMT  
		Size: 5.1 MB (5050667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6212b74a0e2a0bf5776404a542f864df8ecd3e8e346afe06b090b8ad91162ff`  
		Last Modified: Tue, 03 Oct 2023 06:55:59 GMT  
		Size: 1.3 MB (1253059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08077ff6df719127adcc0ba3894d9da76284b6f80691d74d4834c4b3f6749aef`  
		Last Modified: Tue, 03 Oct 2023 06:55:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1db0580f356b0963d41e25dd1069453da372580430ddb463861e3e9beb44b8`  
		Last Modified: Tue, 03 Oct 2023 06:55:56 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d294053e6f8e82d930a66c258ab9ab7805b2bdb4e872947e596fc7ee167e6ed`  
		Last Modified: Tue, 03 Oct 2023 06:55:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2aad3066658018b769c59037aca9d856eedf937ea40b4cc73812f390aec26ac`  
		Last Modified: Tue, 03 Oct 2023 06:56:24 GMT  
		Size: 221.8 MB (221804410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e596cadf5785abc862afdefd06859a7d8188cd7eb73711f0357226d99ecb5db0`  
		Last Modified: Tue, 03 Oct 2023 06:55:57 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:90551a2b189d3e8d1346b538d7c776a816f1d4934a415624e9351e9f4c8054fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250433613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36489d8fed7660cc783b59847b46fe4b7631230854ce7de497d1fdb4c78fa9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:05:20 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Oct 2023 05:05:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:05:30 GMT
ENV GOSU_VERSION=1.16
# Tue, 03 Oct 2023 05:05:30 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 03 Oct 2023 05:05:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 03 Oct 2023 05:05:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 03 Oct 2023 05:05:38 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 03 Oct 2023 05:05:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 03 Oct 2023 05:05:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 03 Oct 2023 05:05:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 03 Oct 2023 05:05:38 GMT
ENV MONGO_MAJOR=7.0
# Tue, 03 Oct 2023 05:05:39 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Oct 2023 05:05:39 GMT
ENV MONGO_VERSION=7.0.2
# Tue, 03 Oct 2023 05:06:00 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Oct 2023 05:06:04 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Oct 2023 05:06:04 GMT
ENV HOME=/data/db
# Tue, 03 Oct 2023 05:06:04 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Tue, 03 Oct 2023 05:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2023 05:06:04 GMT
EXPOSE 27017
# Tue, 03 Oct 2023 05:06:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e7f50dd3203f7b84dc0002961680b684151760bcb368411e9860375243ebaa`  
		Last Modified: Tue, 03 Oct 2023 05:06:59 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515a5b396a1e4dad243802f8309d901c2b854defc42ef3b02f01ff8f3a9b44ac`  
		Last Modified: Tue, 03 Oct 2023 05:07:00 GMT  
		Size: 5.0 MB (4994019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6981979503451cde4f8f32f20ad796e9ec88004b24b0fa20a433941dde3cb9`  
		Last Modified: Tue, 03 Oct 2023 05:07:00 GMT  
		Size: 1.2 MB (1186478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ca81d067655ac8527498c273c9654d825c4dafef6ee63680891bca645c3f06`  
		Last Modified: Tue, 03 Oct 2023 05:06:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92de44e704ff08651f49cdc86c3b3035565545fe02d569005324828f8477482a`  
		Last Modified: Tue, 03 Oct 2023 05:06:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a308d510b7c75226aeed96ee266ecc4349b403695f67eb40ab00b817e9e80ca2`  
		Last Modified: Tue, 03 Oct 2023 05:06:57 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8c8d14739efeee3d9fa9c6560e45e819a4a45f5565719a442b65168047c7c3`  
		Last Modified: Tue, 03 Oct 2023 05:07:17 GMT  
		Size: 215.9 MB (215852359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddcae6a6939e26e9336a41e335a6185bc64825fa06eaf5b198f2af5b898e4ce`  
		Last Modified: Tue, 03 Oct 2023 05:06:58 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
