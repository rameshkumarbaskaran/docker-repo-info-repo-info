## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:a790fbfb3eb04c525575b7681d9d5daf78707633168980595b7dab42bea2d5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:aac6f27030c440d738d3fe8c5e9d36a6f9ceed2c02c35c2d28dfe0628d55bb0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226398638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a440572ac3c10fdc02c51d46a2dcbf3760d10faf3f6a2784054e6e1057f0d92a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 23:28:11 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 02 Feb 2023 23:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Feb 2023 23:28:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 02 Feb 2023 23:28:56 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 02 Feb 2023 23:29:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Feb 2023 23:29:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Feb 2023 23:29:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 02 Feb 2023 23:29:08 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 02 Feb 2023 23:29:08 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 02 Feb 2023 23:29:08 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 02 Feb 2023 23:29:09 GMT
ENV MONGO_MAJOR=6.0
# Thu, 02 Feb 2023 23:29:09 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 02 Feb 2023 23:29:09 GMT
ENV MONGO_VERSION=6.0.4
# Thu, 02 Feb 2023 23:29:29 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 02 Feb 2023 23:29:31 GMT
VOLUME [/data/db /data/configdb]
# Thu, 02 Feb 2023 23:29:31 GMT
ENV HOME=/data/db
# Thu, 02 Feb 2023 23:29:31 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Thu, 02 Feb 2023 23:29:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Feb 2023 23:29:31 GMT
EXPOSE 27017
# Thu, 02 Feb 2023 23:29:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:10ac4908093d4325f2c94b2c9a571fa1071a17a72dd9c21c1ffb2c86f68ca028`  
		Last Modified: Thu, 26 Jan 2023 08:46:26 GMT  
		Size: 30.4 MB (30429004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685504455d092c0ad95e7f34cb4815b245e7598abd7065a555ec529f6ad22ef0`  
		Last Modified: Thu, 02 Feb 2023 23:30:16 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd36404f3293dfe028f31b2dd9d06447a397e6f45db568c38474dcb1a0e2baa`  
		Last Modified: Thu, 02 Feb 2023 23:30:17 GMT  
		Size: 5.0 MB (5027971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abd9b25affb5b65a012e9fedd3074daa71a187649a95ec9190e85b7fbadfd18`  
		Last Modified: Thu, 02 Feb 2023 23:30:16 GMT  
		Size: 1.3 MB (1252435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7fde532eae4fd7e670c75d9a1eff2b3cdb80cf515140482458375bd0a9247e`  
		Last Modified: Thu, 02 Feb 2023 23:30:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc70e4c7d7aac77c526369a692f2546e5f1c64f85e4deda63c4e713e14dafc`  
		Last Modified: Thu, 02 Feb 2023 23:30:14 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc2353072f76bf2f40727482358c69666343f8f1c9b7037a9498d5bee8833b3`  
		Last Modified: Thu, 02 Feb 2023 23:30:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560de8e3a6c780666f845d2bfee66d8374464919ecf4fef169d678ace2a321de`  
		Last Modified: Thu, 02 Feb 2023 23:30:40 GMT  
		Size: 189.7 MB (189680591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0748cd1d792c1bf3d76b7ccaad598f5613c3ae1d9365c7ff6633683a6ea6d278`  
		Last Modified: Thu, 02 Feb 2023 23:30:14 GMT  
		Size: 5.0 KB (4962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:437dcfcd38e72b2d504bb19ad1407619c3bb2191a9f76b51473831628e66287e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229183040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3681738498c404f92569bddcfa0cfb5448561c3f361bb8d4afa32c1ce3b3e566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:47:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:48:01 GMT
ADD file:cf91de9ab30abab112d58c0a7f3bbb35853a02b2e406c65c89430ff049573c47 in / 
# Wed, 01 Mar 2023 04:48:01 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:07:47 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 02 Mar 2023 03:07:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:07:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 02 Mar 2023 03:07:56 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 02 Mar 2023 03:08:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Mar 2023 03:08:04 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Mar 2023 03:08:05 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 02 Mar 2023 03:08:05 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 02 Mar 2023 03:08:05 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 02 Mar 2023 03:08:05 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 02 Mar 2023 03:08:05 GMT
ENV MONGO_MAJOR=6.0
# Thu, 02 Mar 2023 03:08:06 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 02 Mar 2023 03:08:06 GMT
ENV MONGO_VERSION=6.0.4
# Thu, 02 Mar 2023 03:08:24 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 02 Mar 2023 03:08:24 GMT
VOLUME [/data/db /data/configdb]
# Thu, 02 Mar 2023 03:08:24 GMT
ENV HOME=/data/db
# Thu, 02 Mar 2023 03:08:24 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Thu, 02 Mar 2023 03:08:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:08:24 GMT
EXPOSE 27017
# Thu, 02 Mar 2023 03:08:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:986c4f6be3072d9528a459c780295bd053806536d2295a6de6aad327eaf19fad`  
		Last Modified: Wed, 01 Mar 2023 09:02:52 GMT  
		Size: 28.4 MB (28387922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dd2f9a525317253a70d4ae2b96848c13cc05a11d2b6262c501c962da3be5af`  
		Last Modified: Thu, 02 Mar 2023 03:11:10 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa47abefa1943661c33a7d083c7b259925d9601049db144563cbfded420ecd9`  
		Last Modified: Thu, 02 Mar 2023 03:11:10 GMT  
		Size: 5.0 MB (4968513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061fd5097347265b67d628b7d75a74c7022bf716e1ce46c71cbeb4030287b746`  
		Last Modified: Thu, 02 Mar 2023 03:11:10 GMT  
		Size: 1.2 MB (1185058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130857d0db266cbf0cc73053fcde7715f88aa8a51a90980b87272bedd3724173`  
		Last Modified: Thu, 02 Mar 2023 03:11:08 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ed9280970a50edec770dba5b0d264705dd17a4b2a7dd3596325a674455575d`  
		Last Modified: Thu, 02 Mar 2023 03:11:08 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936c45da7e5f21868a60822497b494a1508f9d89caf27c5454020994fdfcead`  
		Last Modified: Thu, 02 Mar 2023 03:11:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d921cae36514aaf97e12564c3c9f81fd340405461636b6d085ff7722659def67`  
		Last Modified: Thu, 02 Mar 2023 03:11:25 GMT  
		Size: 194.6 MB (194632911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdf08f14ccf2d273094645d76bd596ecedfd768b3b9e6b2f1685ece1389ecd4`  
		Last Modified: Thu, 02 Mar 2023 03:11:08 GMT  
		Size: 5.0 KB (4962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
