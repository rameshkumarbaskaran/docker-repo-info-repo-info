## `mongo:jammy`

```console
$ docker pull mongo@sha256:d4288a316c1bb1b4fa2f145c5077e7c25ddcd9acb92160c313a4ffaac1bf4d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:83801634df07132cff11fab970dd54182ebcd39428b1a6bdef02d35ca8328a71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235883503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5e0d0cf6dea27fa96b889dc4687c317f3ff99f582083f2503433d534dfbba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:52:04 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 16 Mar 2023 03:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:52:21 GMT
ENV GOSU_VERSION=1.16
# Thu, 16 Mar 2023 03:52:21 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 16 Mar 2023 03:52:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 16 Mar 2023 03:52:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 16 Mar 2023 03:52:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 16 Mar 2023 03:52:31 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 16 Mar 2023 03:52:31 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 03:52:31 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 03:52:31 GMT
ENV MONGO_MAJOR=6.0
# Thu, 16 Mar 2023 03:52:32 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 16 Mar 2023 03:52:32 GMT
ENV MONGO_VERSION=6.0.5
# Thu, 16 Mar 2023 03:52:50 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 16 Mar 2023 03:52:52 GMT
VOLUME [/data/db /data/configdb]
# Thu, 16 Mar 2023 03:52:52 GMT
ENV HOME=/data/db
# Thu, 16 Mar 2023 03:52:52 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Thu, 16 Mar 2023 03:52:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 03:52:52 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:52:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf92c33f8cbadc8f527c89485639e5d81b86d0f01d8d56020ee93c042352391`  
		Last Modified: Thu, 16 Mar 2023 03:55:37 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad057cae032b18c11a7de4afa11f9351738897fe62149efc6cbae0f19ea84d8`  
		Last Modified: Thu, 16 Mar 2023 03:55:37 GMT  
		Size: 5.0 MB (5027889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94195d632f1b291e7eefdcfe68c73baf2eab2e094d1f37d0b119ba7c6c07aac6`  
		Last Modified: Thu, 16 Mar 2023 03:55:37 GMT  
		Size: 1.3 MB (1252533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a989974eb2ef565acc72b1be59d907047f952ff01db297b690a46dfbddcb3`  
		Last Modified: Thu, 16 Mar 2023 03:55:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94fc3cc2ce1dfbe506c2d4dfc61c83d9c9267a70287100f7a22f72a420f5369`  
		Last Modified: Thu, 16 Mar 2023 03:55:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31c2ebced96b29c89684c7fd03808e74b4f2f4f41b0e260aff39d4f6aa60e8b`  
		Last Modified: Thu, 16 Mar 2023 03:55:35 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af2dc62bb4be045ee020805881f1e6ef86b03683a2174bcfeb6825a7b83ad53`  
		Last Modified: Thu, 16 Mar 2023 03:55:59 GMT  
		Size: 199.2 MB (199164421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5239bce583f11fbc1f8c2a2448d2dc0a0c7d9f94097294bfc908ed047402f8`  
		Last Modified: Thu, 16 Mar 2023 03:55:35 GMT  
		Size: 5.0 KB (5020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:acb204d3254fd64c0474896636a5ad7947ee51534383615e9f4507f9c7e23ab1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230230100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40e61cff6456d27d637fa0e733158f572b1e3b0764ee2a513a63dc5349be8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:36:01 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 03 May 2023 03:46:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:46:38 GMT
ENV GOSU_VERSION=1.16
# Wed, 03 May 2023 03:46:39 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 03 May 2023 03:46:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 03 May 2023 03:46:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 03 May 2023 03:46:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 03 May 2023 03:46:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 03 May 2023 03:46:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 03 May 2023 03:46:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 03 May 2023 03:46:48 GMT
ENV MONGO_MAJOR=6.0
# Wed, 03 May 2023 03:46:49 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 03 May 2023 03:46:49 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 03 May 2023 03:47:05 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 03 May 2023 03:47:08 GMT
VOLUME [/data/db /data/configdb]
# Wed, 03 May 2023 03:47:08 GMT
ENV HOME=/data/db
# Wed, 03 May 2023 03:47:08 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Wed, 03 May 2023 03:47:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 May 2023 03:47:08 GMT
EXPOSE 27017
# Wed, 03 May 2023 03:47:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2217df6bf2b54df86db0fab60f4028346c4e29606fb6319845d946b1ad5e617d`  
		Last Modified: Thu, 16 Mar 2023 02:39:02 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a49be6a81de0299f300b5700fa074a7257fd603f148c5cad390915bd124750`  
		Last Modified: Wed, 03 May 2023 03:50:36 GMT  
		Size: 5.0 MB (4968087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750df30d2691491b8e38f02b8cbffea61fb2fb5642e57dee1f625ad107c3a325`  
		Last Modified: Wed, 03 May 2023 03:50:36 GMT  
		Size: 1.2 MB (1184675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b833fedeb884bfc03730f9c9baf6de6edeea51a44044352d3cc3ab30df38320c`  
		Last Modified: Wed, 03 May 2023 03:50:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0ed224ec45918792f2215a1ba22bbe735b130c374945311370166bad360ae2`  
		Last Modified: Wed, 03 May 2023 03:50:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268969124ed38e48c2b0f48cf12b2a0c0527d67cf77b8bf545badeeb480eb771`  
		Last Modified: Wed, 03 May 2023 03:50:34 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b42bd0409365df88ccad292265ee5d674142b819b3b16789deb1afdbc874183`  
		Last Modified: Wed, 03 May 2023 03:50:51 GMT  
		Size: 195.7 MB (195681084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b81b472a5927d5a0b06914a6b62c7e62b486b523085ec76b3ea9ded5cf4c6c`  
		Last Modified: Wed, 03 May 2023 03:50:34 GMT  
		Size: 5.0 KB (5021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
