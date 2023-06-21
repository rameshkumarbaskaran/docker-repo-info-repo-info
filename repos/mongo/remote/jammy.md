## `mongo:jammy`

```console
$ docker pull mongo@sha256:8cc1853b44958d126478b76ef14baa437415e6b928d3781a2e0f526ae42897b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:aefae4865d1a803f4ffc543bc9b26694025c4faa3517b6dc45c4065e89b6cc7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237400469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e32c3979b029a7f99ed3d3ecfbef3b1ab9c0a373765206f80ded094af1dcbd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:14:50 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 16 Jun 2023 03:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:15:18 GMT
ENV GOSU_VERSION=1.16
# Fri, 16 Jun 2023 03:15:18 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 16 Jun 2023 03:15:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 16 Jun 2023 03:15:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 16 Jun 2023 03:15:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 16 Jun 2023 03:15:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 16 Jun 2023 03:15:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 16 Jun 2023 03:15:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 16 Jun 2023 03:15:48 GMT
ENV MONGO_MAJOR=6.0
# Fri, 16 Jun 2023 03:15:49 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 16 Jun 2023 03:15:49 GMT
ENV MONGO_VERSION=6.0.6
# Fri, 16 Jun 2023 03:16:06 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 16 Jun 2023 03:16:08 GMT
VOLUME [/data/db /data/configdb]
# Fri, 16 Jun 2023 03:16:08 GMT
ENV HOME=/data/db
# Wed, 21 Jun 2023 01:01:57 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 21 Jun 2023 01:01:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jun 2023 01:01:57 GMT
EXPOSE 27017
# Wed, 21 Jun 2023 01:01:57 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5d4dae314d61ef2c7df20dbb6134a5e213a5131de25af242f608e8621368f`  
		Last Modified: Fri, 16 Jun 2023 03:17:58 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe6867b3f800a0cfee1cf1e018de5214b3da298faf0f0e5d6651547c53c765c`  
		Last Modified: Fri, 16 Jun 2023 03:17:59 GMT  
		Size: 5.1 MB (5050584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4c7cb44e892df114bea9e573b88e40ac1e651feb36f91fa6dd91a014f56a7c`  
		Last Modified: Fri, 16 Jun 2023 03:17:58 GMT  
		Size: 1.3 MB (1252923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c7016c15b5571e14f18e728cca49a7f5882fc084cac8412e36d4981757a81f`  
		Last Modified: Fri, 16 Jun 2023 03:17:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d740b6c98119553d4d259f37335119abf517fff019448d1f2cc526e3996ab89`  
		Last Modified: Fri, 16 Jun 2023 03:17:56 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329604f2207885845c2a7dff036e513a28de91883838129f7bae448f71f26aae`  
		Last Modified: Fri, 16 Jun 2023 03:17:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c33622dbce3c03b8edcd622b467ceb1a6d3ad83e20ebd823bcba7993a1c979`  
		Last Modified: Fri, 16 Jun 2023 03:18:21 GMT  
		Size: 200.7 MB (200657263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f7e12b56a3e10b8cd8ca23cad50c0856d89bf8c65711b414e58b8c18003d34`  
		Last Modified: Wed, 21 Jun 2023 01:03:33 GMT  
		Size: 5.0 KB (4992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:5f1d5e7c9d4e76cd685e3d4af61b69f5682cfa4e89d084b1aa4d7448dd870fa7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230960272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f51f8fb299b1f35e44a3fcdfac0d3f39a7223e07b1632a6f546758ed43270c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:28:53 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 16 Jun 2023 03:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:29:02 GMT
ENV GOSU_VERSION=1.16
# Fri, 16 Jun 2023 03:29:02 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 16 Jun 2023 03:29:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 16 Jun 2023 03:29:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 16 Jun 2023 03:29:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 16 Jun 2023 03:29:27 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 16 Jun 2023 03:29:27 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 16 Jun 2023 03:29:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 16 Jun 2023 03:29:28 GMT
ENV MONGO_MAJOR=6.0
# Fri, 16 Jun 2023 03:29:28 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 16 Jun 2023 03:29:28 GMT
ENV MONGO_VERSION=6.0.6
# Fri, 16 Jun 2023 03:29:47 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 16 Jun 2023 03:29:50 GMT
VOLUME [/data/db /data/configdb]
# Fri, 16 Jun 2023 03:29:50 GMT
ENV HOME=/data/db
# Wed, 21 Jun 2023 01:02:48 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 21 Jun 2023 01:02:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jun 2023 01:02:48 GMT
EXPOSE 27017
# Wed, 21 Jun 2023 01:02:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cac3c1cd860738646e8f7907a2c3863a1ee373f9f3831276f505f4fe93848e`  
		Last Modified: Fri, 16 Jun 2023 03:31:24 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4918c863202ff28fd431e919e4f78c35a462692f2a210e2d527f0c79334672d8`  
		Last Modified: Fri, 16 Jun 2023 03:31:24 GMT  
		Size: 5.0 MB (4992702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15db68cff03fa562720903e404ed27b57a3abd31799aadffdd5fdb2240d36451`  
		Last Modified: Fri, 16 Jun 2023 03:31:24 GMT  
		Size: 1.2 MB (1185480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a8d4510bd52238dd307318b241c95bb5047ad5ce42b489d6a68f72efb1576`  
		Last Modified: Fri, 16 Jun 2023 03:31:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81877556e7b413ffc098ea9636438c1788f277520162a9cfef2ab4f42d6120f`  
		Last Modified: Fri, 16 Jun 2023 03:31:22 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7222461baf3a5795081e53a9a91777d9552181b24d41a4d36a9d83110079a8`  
		Last Modified: Fri, 16 Jun 2023 03:31:22 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70685e0a61fdaa99bc51703e7ed9344fdfe38c1ed81ac56fd3a98510bc37efd`  
		Last Modified: Fri, 16 Jun 2023 03:31:39 GMT  
		Size: 196.4 MB (196384219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a36b0e1a54f5ed7f0c6ce039754d662d79e157e36e1a5b58c44afc9b8e6ec49`  
		Last Modified: Wed, 21 Jun 2023 01:04:05 GMT  
		Size: 5.0 KB (4992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
