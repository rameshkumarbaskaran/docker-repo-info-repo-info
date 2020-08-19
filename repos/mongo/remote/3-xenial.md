## `mongo:3-xenial`

```console
$ docker pull mongo@sha256:c5df31943b2a2bbcb09bf22fea82ee6fb46d30059040b1485ba4c2c1500d2475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:465813a0ff3222adbbbfbdb9945d1a86498cd3773cc45e16884ee43a38183fcc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165996688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c0eaedd1b713469c1927425ad61d506dfd74bc2f44c5a4be1925dea60ac20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:39:06 GMT
ADD file:513ae777bc4042f8446c0454f8cffc9a94f8429de963651d9a6dab95d4502007 in / 
# Fri, 24 Jul 2020 14:39:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:39:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:39:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:39:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:27:03 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:27:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:27:11 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:27:11 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:27:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:27:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:27:24 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Jul 2020 16:27:24 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:27:25 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:27:25 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:25 GMT
ENV MONGO_MAJOR=3.6
# Fri, 24 Jul 2020 16:27:25 GMT
ENV MONGO_VERSION=3.6.19
# Fri, 24 Jul 2020 16:27:26 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:27:43 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:27:44 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:27:44 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:27:44 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:27:44 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:27:44 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7b378fa0f9085667ced1c76c9919cde8663becf2218e8d20e2df8d0824311531`  
		Last Modified: Tue, 07 Jul 2020 13:19:56 GMT  
		Size: 44.4 MB (44401021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d77b1b29f2e9b6f141b9d8f74b601f40eb998544783f4a0a3cdc384873c1a4e`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c793be88baee3f3204444e4d4e49c4e44c1709d40182c131cd5681c94e17227`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc05c8a19c0cf83f2f44263c967c3fe81fffc4b41b592ad088fb1534c206e70`  
		Last Modified: Fri, 24 Jul 2020 14:39:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94562b188f30b535033d3769cfa23f701b272d320288b7eadb72cb87fa99619`  
		Last Modified: Fri, 24 Jul 2020 16:29:56 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006d818b06b0bccfd9c0820466c5053250970cd58606cf19498582d59edd3440`  
		Last Modified: Fri, 24 Jul 2020 16:29:56 GMT  
		Size: 2.9 MB (2904053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c90f20ca83ccd3b4dc91520476bdff3a9ff24957b13ceed54c05cfb323cab4`  
		Last Modified: Fri, 24 Jul 2020 16:29:56 GMT  
		Size: 1.3 MB (1305133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eecb12b08f4a6666fc27782720b8d4070173f552f9d73b522e96c8e4bf2e8da`  
		Last Modified: Fri, 24 Jul 2020 16:29:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47cbb1ec754c4014b2d584ed0ae5e9b85391a51d46e09a87840ee6f79b6a602`  
		Last Modified: Fri, 24 Jul 2020 16:29:54 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a87ed0237df53998e01da22fc4716df1cc686d05334741afa4c59bd7767d597`  
		Last Modified: Fri, 24 Jul 2020 16:29:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374abc24cac18cffb21f357dc3c2d5f0fff7f9c59eb75b5f8337b71d23244e82`  
		Last Modified: Fri, 24 Jul 2020 16:30:13 GMT  
		Size: 117.4 MB (117376512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04946784f1e8cf96407ea7fe9d08c8744a72ddcc5d4f0f7427987e2f275722d`  
		Last Modified: Fri, 24 Jul 2020 16:29:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476068d5a49857204be2f39c3e20e927ea4e953a8320b98b78a18c3cf3a95a01`  
		Last Modified: Fri, 24 Jul 2020 16:29:54 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:c0ae3888736d69a12caa6c43b40170b51425cfdf79fa3681f4540861576fce18
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155338889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2909f7bf21269c9924ca0c2fa73fc710372552ed29206981463832ceab617d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 19 Aug 2020 21:31:42 GMT
ADD file:20ffb81d6b7edd3826c028369ed1774914394328d1ccef79ecee109f5cfbcc5f in / 
# Wed, 19 Aug 2020 21:31:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:31:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:31:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:31:52 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:31:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 19 Aug 2020 22:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:32:15 GMT
ENV GOSU_VERSION=1.12
# Wed, 19 Aug 2020 22:32:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 19 Aug 2020 22:32:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 19 Aug 2020 22:32:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 19 Aug 2020 22:32:47 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 19 Aug 2020 22:32:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 19 Aug 2020 22:32:51 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 19 Aug 2020 22:32:52 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 19 Aug 2020 22:32:53 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 19 Aug 2020 22:32:53 GMT
ENV MONGO_MAJOR=3.6
# Wed, 19 Aug 2020 22:32:54 GMT
ENV MONGO_VERSION=3.6.19
# Wed, 19 Aug 2020 22:32:55 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 19 Aug 2020 22:33:18 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 19 Aug 2020 22:33:22 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 19 Aug 2020 22:33:23 GMT
VOLUME [/data/db /data/configdb]
# Wed, 19 Aug 2020 22:33:24 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 19 Aug 2020 22:33:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Aug 2020 22:33:26 GMT
EXPOSE 27017
# Wed, 19 Aug 2020 22:33:26 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3266c9b0302777bdc8ccdffab895ef058fb0777dc7600b0fe0b6c80dd3e71f9b`  
		Last Modified: Sat, 08 Aug 2020 00:25:28 GMT  
		Size: 40.1 MB (40073893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5240d1a89e17ed7dda51e3b38d3749e4ab3fb2fc2433de69ea23a838bb00c7`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be065fa7bcd4d9f2540e1fec00c455a04755974444b17fb108b73cd4b15963a1`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75305dc60d93c15276fd1b3dc21a09ef1ce9c248393c85eb1a5caf2be6e02671`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e57371bd09af15391debc536f6839de7e6ebe7295d50c757dd90f1df6a30da`  
		Last Modified: Wed, 19 Aug 2020 22:37:42 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b81baa9ce507ec53d3e562d07f480173afa304930494fbd5016ce1c973d8a7`  
		Last Modified: Wed, 19 Aug 2020 22:37:42 GMT  
		Size: 2.4 MB (2432322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0017ea2c2557a608f31f58299936c07c02b7ace3893a5023ca8cad1251034d`  
		Last Modified: Wed, 19 Aug 2020 22:37:42 GMT  
		Size: 1.2 MB (1232551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7d1adbe02e2dba2f95d6a9d5b4e8b7282501efd56540440feebb899992e8b1`  
		Last Modified: Wed, 19 Aug 2020 22:37:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec57e97f591b600e564b6e8987f319c18ba7a51c04e3fa1f57cb379b5925dd1`  
		Last Modified: Wed, 19 Aug 2020 22:37:39 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29758a89cbd002946903ddf1bb164da5e54f6ee672fc1bbd9757aa6e6a9489db`  
		Last Modified: Wed, 19 Aug 2020 22:37:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba9aeebb1082432123096ff49b22c17906659291e2932c7ef81825d5f5f2bbc`  
		Last Modified: Wed, 19 Aug 2020 22:38:18 GMT  
		Size: 111.6 MB (111590125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb536ab7200c7b9051ccf226346ab245dcae3ff7680246249aefb822d3a1da84`  
		Last Modified: Wed, 19 Aug 2020 22:37:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa474c7c76ae49118086d377ef5d0fe8a4671a0cf1db2f13a351d64dd17c747`  
		Last Modified: Wed, 19 Aug 2020 22:37:39 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
