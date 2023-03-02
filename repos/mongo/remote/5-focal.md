## `mongo:5-focal`

```console
$ docker pull mongo@sha256:2519065db7151d92129a27b450519adb99f0c35323ef9516b00164423f87ccf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:bc4f10b257081511cbd88e93377416894b14c6ba46b2e58fc855d88045c367f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251104169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ef950caaf86fc4bdff4e19420acf42cc6df6c82173ad789a37273d7a20bbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:26:06 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 01 Feb 2023 19:26:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:26:21 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 19:26:21 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 01 Feb 2023 19:26:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 19:26:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 01 Feb 2023 19:27:04 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 19:27:05 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 01 Feb 2023 19:27:05 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 01 Feb 2023 19:27:05 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 01 Feb 2023 19:27:05 GMT
ENV MONGO_MAJOR=5.0
# Wed, 01 Feb 2023 19:27:05 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 25 Feb 2023 00:37:33 GMT
ENV MONGO_VERSION=5.0.15
# Sat, 25 Feb 2023 00:38:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 25 Feb 2023 00:38:05 GMT
VOLUME [/data/db /data/configdb]
# Sat, 25 Feb 2023 00:38:05 GMT
ENV HOME=/data/db
# Sat, 25 Feb 2023 00:38:05 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Sat, 25 Feb 2023 00:38:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 25 Feb 2023 00:38:05 GMT
EXPOSE 27017
# Sat, 25 Feb 2023 00:38:05 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7638a79c68d650ad78bf1c04cbc9ef160606e02e19fcdfc357d3a49d9f3dfb`  
		Last Modified: Wed, 01 Feb 2023 19:29:02 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edb8e32447e402814b615208f1a93870bff3994e2b654ae16c438879bc31277`  
		Last Modified: Wed, 01 Feb 2023 19:29:03 GMT  
		Size: 8.3 MB (8348522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b078a16e980d806afa564ded9aaef5b7cf74b44a75880db13e1912297a6bc0c`  
		Last Modified: Wed, 01 Feb 2023 19:29:02 GMT  
		Size: 1.3 MB (1255800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09083ae98273683297e023dfe39760a10a453891715f75c451db8f0916beecd`  
		Last Modified: Wed, 01 Feb 2023 19:29:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d64b6b8a202c58544a68188edb02828e522b2d84d35a1a91962fc6f5a03bb06`  
		Last Modified: Wed, 01 Feb 2023 19:29:41 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e34d62e5cec276034d5d75f5ab5952d86c070d81f6f2885b0a9231bc3b3011e`  
		Last Modified: Wed, 01 Feb 2023 19:29:41 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439b8e6e66a4b36f4c19e8323b4812f07547cc3a6681971ad9225c881ed418c2`  
		Last Modified: Sat, 25 Feb 2023 00:39:53 GMT  
		Size: 212.9 MB (212913318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8178acfc9a685a4fb7f0cd81c32a1d63fa75b8d7e4f338563217fc568baf8ddd`  
		Last Modified: Sat, 25 Feb 2023 00:39:28 GMT  
		Size: 5.0 KB (4959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2d4abe15756a67258bad0c19ab5e29d2e2b899eedefc9a90327c46537e2b3691
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246841227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e089e674577101e312cf29ab586c3dff9645cc3c97f68a954f65222514bb57a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:08:35 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 02 Mar 2023 03:08:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:08:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 02 Mar 2023 03:08:44 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 02 Mar 2023 03:08:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Mar 2023 03:08:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Mar 2023 03:08:52 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 02 Mar 2023 03:08:52 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 02 Mar 2023 03:08:52 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 02 Mar 2023 03:08:52 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 02 Mar 2023 03:08:52 GMT
ENV MONGO_MAJOR=5.0
# Thu, 02 Mar 2023 03:08:52 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 02 Mar 2023 03:08:53 GMT
ENV MONGO_VERSION=5.0.15
# Thu, 02 Mar 2023 03:09:10 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 02 Mar 2023 03:09:13 GMT
VOLUME [/data/db /data/configdb]
# Thu, 02 Mar 2023 03:09:13 GMT
ENV HOME=/data/db
# Thu, 02 Mar 2023 03:09:13 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Thu, 02 Mar 2023 03:09:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:09:13 GMT
EXPOSE 27017
# Thu, 02 Mar 2023 03:09:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e28cabe5b8f281103472572c0e399c29fbf74223424938ede3ad075366c54a4`  
		Last Modified: Thu, 02 Mar 2023 03:11:41 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fe96ecdce59379bca8bb02a9459cf43ba1986a9088a6662eb99c7fec20edcd`  
		Last Modified: Thu, 02 Mar 2023 03:11:42 GMT  
		Size: 8.2 MB (8179205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ff04ba7a2ec5f3105430e627489f080663eda132ffbc69f28c76208b08392`  
		Last Modified: Thu, 02 Mar 2023 03:11:41 GMT  
		Size: 1.2 MB (1188294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81d49462d00fb935bb228aa8e73eb44f3b1a61118c624a67376a34e6b60201a`  
		Last Modified: Thu, 02 Mar 2023 03:11:39 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a4ec657a0fd71ca7cfa0358c86b3565f44c16bda114f55d86624148c8b93a`  
		Last Modified: Thu, 02 Mar 2023 03:11:39 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5b2b77b2048be78514638e156d88bb5849d87ac02e25a0858de0611a8afccd`  
		Last Modified: Thu, 02 Mar 2023 03:11:39 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b540ece9903d199c48b66b1773cab0369c56825ed2a66769aa86c26b41c4c2b`  
		Last Modified: Thu, 02 Mar 2023 03:11:57 GMT  
		Size: 210.3 MB (210270558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869745c8768c9759f33fffed5bf71308c562c5121c36b8a8d95012ae31e53e09`  
		Last Modified: Thu, 02 Mar 2023 03:11:39 GMT  
		Size: 5.0 KB (4965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
