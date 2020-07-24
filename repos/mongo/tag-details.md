<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo`

-	[`mongo:3`](#mongo3)
-	[`mongo:3.6`](#mongo36)
-	[`mongo:3.6.19`](#mongo3619)
-	[`mongo:3.6.19-windowsservercore`](#mongo3619-windowsservercore)
-	[`mongo:3.6.19-windowsservercore-1809`](#mongo3619-windowsservercore-1809)
-	[`mongo:3.6.19-windowsservercore-ltsc2016`](#mongo3619-windowsservercore-ltsc2016)
-	[`mongo:3.6.19-xenial`](#mongo3619-xenial)
-	[`mongo:3.6-windowsservercore`](#mongo36-windowsservercore)
-	[`mongo:3.6-windowsservercore-1809`](#mongo36-windowsservercore-1809)
-	[`mongo:3.6-windowsservercore-ltsc2016`](#mongo36-windowsservercore-ltsc2016)
-	[`mongo:3.6-xenial`](#mongo36-xenial)
-	[`mongo:3-windowsservercore`](#mongo3-windowsservercore)
-	[`mongo:3-windowsservercore-1809`](#mongo3-windowsservercore-1809)
-	[`mongo:3-windowsservercore-ltsc2016`](#mongo3-windowsservercore-ltsc2016)
-	[`mongo:3-xenial`](#mongo3-xenial)
-	[`mongo:4`](#mongo4)
-	[`mongo:4.0`](#mongo40)
-	[`mongo:4.0.19`](#mongo4019)
-	[`mongo:4.0.19-windowsservercore`](#mongo4019-windowsservercore)
-	[`mongo:4.0.19-windowsservercore-1809`](#mongo4019-windowsservercore-1809)
-	[`mongo:4.0.19-windowsservercore-ltsc2016`](#mongo4019-windowsservercore-ltsc2016)
-	[`mongo:4.0.19-xenial`](#mongo4019-xenial)
-	[`mongo:4.0-windowsservercore`](#mongo40-windowsservercore)
-	[`mongo:4.0-windowsservercore-1809`](#mongo40-windowsservercore-1809)
-	[`mongo:4.0-windowsservercore-ltsc2016`](#mongo40-windowsservercore-ltsc2016)
-	[`mongo:4.0-xenial`](#mongo40-xenial)
-	[`mongo:4.2`](#mongo42)
-	[`mongo:4.2.8`](#mongo428)
-	[`mongo:4.2.8-bionic`](#mongo428-bionic)
-	[`mongo:4.2.8-windowsservercore`](#mongo428-windowsservercore)
-	[`mongo:4.2.8-windowsservercore-1809`](#mongo428-windowsservercore-1809)
-	[`mongo:4.2.8-windowsservercore-ltsc2016`](#mongo428-windowsservercore-ltsc2016)
-	[`mongo:4.2-bionic`](#mongo42-bionic)
-	[`mongo:4.2-windowsservercore`](#mongo42-windowsservercore)
-	[`mongo:4.2-windowsservercore-1809`](#mongo42-windowsservercore-1809)
-	[`mongo:4.2-windowsservercore-ltsc2016`](#mongo42-windowsservercore-ltsc2016)
-	[`mongo:4.4.0-rc14`](#mongo440-rc14)
-	[`mongo:4.4.0-rc14-bionic`](#mongo440-rc14-bionic)
-	[`mongo:4.4.0-rc14-windowsservercore`](#mongo440-rc14-windowsservercore)
-	[`mongo:4.4.0-rc14-windowsservercore-1809`](#mongo440-rc14-windowsservercore-1809)
-	[`mongo:4.4.0-rc14-windowsservercore-ltsc2016`](#mongo440-rc14-windowsservercore-ltsc2016)
-	[`mongo:4.4-rc`](#mongo44-rc)
-	[`mongo:4.4-rc-bionic`](#mongo44-rc-bionic)
-	[`mongo:4.4-rc-windowsservercore`](#mongo44-rc-windowsservercore)
-	[`mongo:4.4-rc-windowsservercore-1809`](#mongo44-rc-windowsservercore-1809)
-	[`mongo:4.4-rc-windowsservercore-ltsc2016`](#mongo44-rc-windowsservercore-ltsc2016)
-	[`mongo:4-bionic`](#mongo4-bionic)
-	[`mongo:4-windowsservercore`](#mongo4-windowsservercore)
-	[`mongo:4-windowsservercore-1809`](#mongo4-windowsservercore-1809)
-	[`mongo:4-windowsservercore-ltsc2016`](#mongo4-windowsservercore-ltsc2016)
-	[`mongo:bionic`](#mongobionic)
-	[`mongo:latest`](#mongolatest)
-	[`mongo:windowsservercore`](#mongowindowsservercore)
-	[`mongo:windowsservercore-1809`](#mongowindowsservercore-1809)
-	[`mongo:windowsservercore-ltsc2016`](#mongowindowsservercore-ltsc2016)

## `mongo:3`

```console
$ docker pull mongo@sha256:db0faea82dd78825be7d9a055d382106c36913fd3f5836da5fd21413de4107ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:3` - linux; amd64

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

### `mongo:3` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a6836de068e015e48898dd2a7f99139fd42153e9d521e077886a9f348eb4155d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155299204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a4b09162e7b7dde2a56907a2a0080f8d03b37bae2b2fd6390e3628837656ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:13:18 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:13:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:23 GMT
ENV MONGO_MAJOR=3.6
# Thu, 23 Jul 2020 18:44:54 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:45:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:45:54 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:46:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:46:08 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:46:09 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:46:11 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:46:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49fdddd7a4914963d409db49a451fab9f30114008fd6b3ab0a51483037fbd6c`  
		Last Modified: Mon, 06 Jul 2020 22:18:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1b7f0f3995be98399c02ad4abb2a3c35046c968c1e1b8219eaa8348a697af0`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f7d29c745886e2285d8c042322d2d2cd0b84a04ae5771f21ca1450383769c8`  
		Last Modified: Thu, 23 Jul 2020 18:49:02 GMT  
		Size: 111.6 MB (111589719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51adc290322c881bbe789cdc57dc04f174af859323617dd0c751f885853fa3c`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4216d9ee2bf67337acbb8059de2e7063f42e79bfdbcc73c28b05e25daca026f7`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:7d4ab7df572f0d08a460d1fd24cc055a123f9cf6f8e1392fcb071aa3bb3d55a7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193316007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd386f37818d2ce37556036f90be88c80e05ad76e37608c26ebeb95648d5f86c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:41:35 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:41:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:41:38 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 18:58:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 18:58:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 18:58:32 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:58:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b67fbc3e5b36bd6602f2bfe0ee3e651234b80d90fadf2cf999749df2b40b27`  
		Last Modified: Thu, 23 Jul 2020 19:50:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a970e681d343ba286f519cb4ec238e076b07a7cfec4987e63d7d745347e60bd6`  
		Last Modified: Thu, 23 Jul 2020 19:50:06 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ed0f529cad4a8db22d58adc6c46b334cc83b696c99b3c671d5f803be00012`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc504f49399ad2198c7515cd1dc3438ecea31852f6f74ae3d66382469df7be0d`  
		Last Modified: Thu, 23 Jul 2020 19:51:00 GMT  
		Size: 455.8 MB (455846002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3d470189184407166c665554c86a97eeb245bcab47d55ea4e4c7396abc22b`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8586d73bdd27bddbb9c0c0265f41c60c1f8881b7909439400255e30e8d346a74`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008d6bf82ea1808f76b8569f83138d86a650a5ac78eafbffc32ff1c077a00e1`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:b97692594e0f23c58d1859d12e9515c8098f48c1a9ad6d17a50b1459f24da483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765492418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec7e890456c17b703dd39619addc9083928532e1b338551d13fca1f6ecf5b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:58:40 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:58:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:58:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 19:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:16:37 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:16:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bdae619d05db985c39b6ad49966019e7d3c53af0634697ce48984c62f28fa0`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4632cb3564f900163ab50d3acff20af90b8b27ae2495c91cf10fa2e0b02a2d8a`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3cd801f45fc0b7c8549109691f233c31a5ef9f2584899b59149e815e4cd6ec`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b03a831dc89ff2b94de9869ffafb4bd0f8d6d0534e777e4a6b924460c4971`  
		Last Modified: Thu, 23 Jul 2020 19:52:09 GMT  
		Size: 455.3 MB (455292150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa03bd57a8e83a36089fd27aec8731143f1fdfbfd35a6ea556a6c05ba3cf17`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166dd50f9c2e72c7dc4dc8772f70619d493b54a5e6e94ba20cfc66b090216a1`  
		Last Modified: Thu, 23 Jul 2020 19:51:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09663ebe0bc752ca2a2dbf19987d0d1eec4d0ed3c1355da55c27fca8d4b1066`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6`

```console
$ docker pull mongo@sha256:db0faea82dd78825be7d9a055d382106c36913fd3f5836da5fd21413de4107ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:3.6` - linux; amd64

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

### `mongo:3.6` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a6836de068e015e48898dd2a7f99139fd42153e9d521e077886a9f348eb4155d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155299204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a4b09162e7b7dde2a56907a2a0080f8d03b37bae2b2fd6390e3628837656ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:13:18 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:13:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:23 GMT
ENV MONGO_MAJOR=3.6
# Thu, 23 Jul 2020 18:44:54 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:45:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:45:54 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:46:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:46:08 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:46:09 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:46:11 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:46:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49fdddd7a4914963d409db49a451fab9f30114008fd6b3ab0a51483037fbd6c`  
		Last Modified: Mon, 06 Jul 2020 22:18:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1b7f0f3995be98399c02ad4abb2a3c35046c968c1e1b8219eaa8348a697af0`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f7d29c745886e2285d8c042322d2d2cd0b84a04ae5771f21ca1450383769c8`  
		Last Modified: Thu, 23 Jul 2020 18:49:02 GMT  
		Size: 111.6 MB (111589719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51adc290322c881bbe789cdc57dc04f174af859323617dd0c751f885853fa3c`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4216d9ee2bf67337acbb8059de2e7063f42e79bfdbcc73c28b05e25daca026f7`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:7d4ab7df572f0d08a460d1fd24cc055a123f9cf6f8e1392fcb071aa3bb3d55a7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193316007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd386f37818d2ce37556036f90be88c80e05ad76e37608c26ebeb95648d5f86c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:41:35 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:41:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:41:38 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 18:58:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 18:58:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 18:58:32 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:58:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b67fbc3e5b36bd6602f2bfe0ee3e651234b80d90fadf2cf999749df2b40b27`  
		Last Modified: Thu, 23 Jul 2020 19:50:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a970e681d343ba286f519cb4ec238e076b07a7cfec4987e63d7d745347e60bd6`  
		Last Modified: Thu, 23 Jul 2020 19:50:06 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ed0f529cad4a8db22d58adc6c46b334cc83b696c99b3c671d5f803be00012`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc504f49399ad2198c7515cd1dc3438ecea31852f6f74ae3d66382469df7be0d`  
		Last Modified: Thu, 23 Jul 2020 19:51:00 GMT  
		Size: 455.8 MB (455846002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3d470189184407166c665554c86a97eeb245bcab47d55ea4e4c7396abc22b`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8586d73bdd27bddbb9c0c0265f41c60c1f8881b7909439400255e30e8d346a74`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008d6bf82ea1808f76b8569f83138d86a650a5ac78eafbffc32ff1c077a00e1`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:b97692594e0f23c58d1859d12e9515c8098f48c1a9ad6d17a50b1459f24da483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765492418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec7e890456c17b703dd39619addc9083928532e1b338551d13fca1f6ecf5b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:58:40 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:58:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:58:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 19:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:16:37 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:16:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bdae619d05db985c39b6ad49966019e7d3c53af0634697ce48984c62f28fa0`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4632cb3564f900163ab50d3acff20af90b8b27ae2495c91cf10fa2e0b02a2d8a`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3cd801f45fc0b7c8549109691f233c31a5ef9f2584899b59149e815e4cd6ec`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b03a831dc89ff2b94de9869ffafb4bd0f8d6d0534e777e4a6b924460c4971`  
		Last Modified: Thu, 23 Jul 2020 19:52:09 GMT  
		Size: 455.3 MB (455292150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa03bd57a8e83a36089fd27aec8731143f1fdfbfd35a6ea556a6c05ba3cf17`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166dd50f9c2e72c7dc4dc8772f70619d493b54a5e6e94ba20cfc66b090216a1`  
		Last Modified: Thu, 23 Jul 2020 19:51:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09663ebe0bc752ca2a2dbf19987d0d1eec4d0ed3c1355da55c27fca8d4b1066`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.19`

```console
$ docker pull mongo@sha256:db0faea82dd78825be7d9a055d382106c36913fd3f5836da5fd21413de4107ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:3.6.19` - linux; amd64

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

### `mongo:3.6.19` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a6836de068e015e48898dd2a7f99139fd42153e9d521e077886a9f348eb4155d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155299204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a4b09162e7b7dde2a56907a2a0080f8d03b37bae2b2fd6390e3628837656ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:13:18 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:13:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:23 GMT
ENV MONGO_MAJOR=3.6
# Thu, 23 Jul 2020 18:44:54 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:45:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:45:54 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:46:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:46:08 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:46:09 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:46:11 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:46:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49fdddd7a4914963d409db49a451fab9f30114008fd6b3ab0a51483037fbd6c`  
		Last Modified: Mon, 06 Jul 2020 22:18:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1b7f0f3995be98399c02ad4abb2a3c35046c968c1e1b8219eaa8348a697af0`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f7d29c745886e2285d8c042322d2d2cd0b84a04ae5771f21ca1450383769c8`  
		Last Modified: Thu, 23 Jul 2020 18:49:02 GMT  
		Size: 111.6 MB (111589719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51adc290322c881bbe789cdc57dc04f174af859323617dd0c751f885853fa3c`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4216d9ee2bf67337acbb8059de2e7063f42e79bfdbcc73c28b05e25daca026f7`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.19` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:7d4ab7df572f0d08a460d1fd24cc055a123f9cf6f8e1392fcb071aa3bb3d55a7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193316007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd386f37818d2ce37556036f90be88c80e05ad76e37608c26ebeb95648d5f86c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:41:35 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:41:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:41:38 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 18:58:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 18:58:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 18:58:32 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:58:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b67fbc3e5b36bd6602f2bfe0ee3e651234b80d90fadf2cf999749df2b40b27`  
		Last Modified: Thu, 23 Jul 2020 19:50:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a970e681d343ba286f519cb4ec238e076b07a7cfec4987e63d7d745347e60bd6`  
		Last Modified: Thu, 23 Jul 2020 19:50:06 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ed0f529cad4a8db22d58adc6c46b334cc83b696c99b3c671d5f803be00012`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc504f49399ad2198c7515cd1dc3438ecea31852f6f74ae3d66382469df7be0d`  
		Last Modified: Thu, 23 Jul 2020 19:51:00 GMT  
		Size: 455.8 MB (455846002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3d470189184407166c665554c86a97eeb245bcab47d55ea4e4c7396abc22b`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8586d73bdd27bddbb9c0c0265f41c60c1f8881b7909439400255e30e8d346a74`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008d6bf82ea1808f76b8569f83138d86a650a5ac78eafbffc32ff1c077a00e1`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.19` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:b97692594e0f23c58d1859d12e9515c8098f48c1a9ad6d17a50b1459f24da483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765492418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec7e890456c17b703dd39619addc9083928532e1b338551d13fca1f6ecf5b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:58:40 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:58:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:58:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 19:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:16:37 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:16:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bdae619d05db985c39b6ad49966019e7d3c53af0634697ce48984c62f28fa0`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4632cb3564f900163ab50d3acff20af90b8b27ae2495c91cf10fa2e0b02a2d8a`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3cd801f45fc0b7c8549109691f233c31a5ef9f2584899b59149e815e4cd6ec`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b03a831dc89ff2b94de9869ffafb4bd0f8d6d0534e777e4a6b924460c4971`  
		Last Modified: Thu, 23 Jul 2020 19:52:09 GMT  
		Size: 455.3 MB (455292150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa03bd57a8e83a36089fd27aec8731143f1fdfbfd35a6ea556a6c05ba3cf17`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166dd50f9c2e72c7dc4dc8772f70619d493b54a5e6e94ba20cfc66b090216a1`  
		Last Modified: Thu, 23 Jul 2020 19:51:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09663ebe0bc752ca2a2dbf19987d0d1eec4d0ed3c1355da55c27fca8d4b1066`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.19-windowsservercore`

```console
$ docker pull mongo@sha256:5c505f940177ca5cce5e4ae91ea8a755d94bd15f9df9ad0bbbdb9d0bbeecf2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:3.6.19-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:7d4ab7df572f0d08a460d1fd24cc055a123f9cf6f8e1392fcb071aa3bb3d55a7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193316007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd386f37818d2ce37556036f90be88c80e05ad76e37608c26ebeb95648d5f86c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:41:35 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:41:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:41:38 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 18:58:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 18:58:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 18:58:32 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:58:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b67fbc3e5b36bd6602f2bfe0ee3e651234b80d90fadf2cf999749df2b40b27`  
		Last Modified: Thu, 23 Jul 2020 19:50:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a970e681d343ba286f519cb4ec238e076b07a7cfec4987e63d7d745347e60bd6`  
		Last Modified: Thu, 23 Jul 2020 19:50:06 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ed0f529cad4a8db22d58adc6c46b334cc83b696c99b3c671d5f803be00012`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc504f49399ad2198c7515cd1dc3438ecea31852f6f74ae3d66382469df7be0d`  
		Last Modified: Thu, 23 Jul 2020 19:51:00 GMT  
		Size: 455.8 MB (455846002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3d470189184407166c665554c86a97eeb245bcab47d55ea4e4c7396abc22b`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8586d73bdd27bddbb9c0c0265f41c60c1f8881b7909439400255e30e8d346a74`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008d6bf82ea1808f76b8569f83138d86a650a5ac78eafbffc32ff1c077a00e1`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.19-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:b97692594e0f23c58d1859d12e9515c8098f48c1a9ad6d17a50b1459f24da483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765492418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec7e890456c17b703dd39619addc9083928532e1b338551d13fca1f6ecf5b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:58:40 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:58:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:58:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 19:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:16:37 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:16:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bdae619d05db985c39b6ad49966019e7d3c53af0634697ce48984c62f28fa0`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4632cb3564f900163ab50d3acff20af90b8b27ae2495c91cf10fa2e0b02a2d8a`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3cd801f45fc0b7c8549109691f233c31a5ef9f2584899b59149e815e4cd6ec`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b03a831dc89ff2b94de9869ffafb4bd0f8d6d0534e777e4a6b924460c4971`  
		Last Modified: Thu, 23 Jul 2020 19:52:09 GMT  
		Size: 455.3 MB (455292150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa03bd57a8e83a36089fd27aec8731143f1fdfbfd35a6ea556a6c05ba3cf17`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166dd50f9c2e72c7dc4dc8772f70619d493b54a5e6e94ba20cfc66b090216a1`  
		Last Modified: Thu, 23 Jul 2020 19:51:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09663ebe0bc752ca2a2dbf19987d0d1eec4d0ed3c1355da55c27fca8d4b1066`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.19-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a8c621c7837356a751efad96caeb95f7611a19fa242573be440fadddadc70d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:3.6.19-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:b97692594e0f23c58d1859d12e9515c8098f48c1a9ad6d17a50b1459f24da483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765492418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec7e890456c17b703dd39619addc9083928532e1b338551d13fca1f6ecf5b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:58:40 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:58:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:58:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 19:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:16:37 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:16:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bdae619d05db985c39b6ad49966019e7d3c53af0634697ce48984c62f28fa0`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4632cb3564f900163ab50d3acff20af90b8b27ae2495c91cf10fa2e0b02a2d8a`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3cd801f45fc0b7c8549109691f233c31a5ef9f2584899b59149e815e4cd6ec`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b03a831dc89ff2b94de9869ffafb4bd0f8d6d0534e777e4a6b924460c4971`  
		Last Modified: Thu, 23 Jul 2020 19:52:09 GMT  
		Size: 455.3 MB (455292150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa03bd57a8e83a36089fd27aec8731143f1fdfbfd35a6ea556a6c05ba3cf17`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166dd50f9c2e72c7dc4dc8772f70619d493b54a5e6e94ba20cfc66b090216a1`  
		Last Modified: Thu, 23 Jul 2020 19:51:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09663ebe0bc752ca2a2dbf19987d0d1eec4d0ed3c1355da55c27fca8d4b1066`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.19-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:3856215bb112e8077ebb95b8847918cc83446cbdeab132daba9e319c91fafdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:3.6.19-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:7d4ab7df572f0d08a460d1fd24cc055a123f9cf6f8e1392fcb071aa3bb3d55a7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193316007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd386f37818d2ce37556036f90be88c80e05ad76e37608c26ebeb95648d5f86c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:41:35 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:41:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:41:38 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 18:58:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 18:58:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 18:58:32 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:58:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b67fbc3e5b36bd6602f2bfe0ee3e651234b80d90fadf2cf999749df2b40b27`  
		Last Modified: Thu, 23 Jul 2020 19:50:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a970e681d343ba286f519cb4ec238e076b07a7cfec4987e63d7d745347e60bd6`  
		Last Modified: Thu, 23 Jul 2020 19:50:06 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ed0f529cad4a8db22d58adc6c46b334cc83b696c99b3c671d5f803be00012`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc504f49399ad2198c7515cd1dc3438ecea31852f6f74ae3d66382469df7be0d`  
		Last Modified: Thu, 23 Jul 2020 19:51:00 GMT  
		Size: 455.8 MB (455846002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3d470189184407166c665554c86a97eeb245bcab47d55ea4e4c7396abc22b`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8586d73bdd27bddbb9c0c0265f41c60c1f8881b7909439400255e30e8d346a74`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008d6bf82ea1808f76b8569f83138d86a650a5ac78eafbffc32ff1c077a00e1`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.19-xenial`

```console
$ docker pull mongo@sha256:75c7759e6213d1e5b9575a7e2b47d53c15418957bc4d316a9a001d0f5ceeb5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6.19-xenial` - linux; amd64

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

### `mongo:3.6.19-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a6836de068e015e48898dd2a7f99139fd42153e9d521e077886a9f348eb4155d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155299204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a4b09162e7b7dde2a56907a2a0080f8d03b37bae2b2fd6390e3628837656ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:13:18 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:13:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:23 GMT
ENV MONGO_MAJOR=3.6
# Thu, 23 Jul 2020 18:44:54 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:45:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:45:54 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:46:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:46:08 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:46:09 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:46:11 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:46:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49fdddd7a4914963d409db49a451fab9f30114008fd6b3ab0a51483037fbd6c`  
		Last Modified: Mon, 06 Jul 2020 22:18:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1b7f0f3995be98399c02ad4abb2a3c35046c968c1e1b8219eaa8348a697af0`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f7d29c745886e2285d8c042322d2d2cd0b84a04ae5771f21ca1450383769c8`  
		Last Modified: Thu, 23 Jul 2020 18:49:02 GMT  
		Size: 111.6 MB (111589719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51adc290322c881bbe789cdc57dc04f174af859323617dd0c751f885853fa3c`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4216d9ee2bf67337acbb8059de2e7063f42e79bfdbcc73c28b05e25daca026f7`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore`

```console
$ docker pull mongo@sha256:5c505f940177ca5cce5e4ae91ea8a755d94bd15f9df9ad0bbbdb9d0bbeecf2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:3.6-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:7d4ab7df572f0d08a460d1fd24cc055a123f9cf6f8e1392fcb071aa3bb3d55a7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193316007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd386f37818d2ce37556036f90be88c80e05ad76e37608c26ebeb95648d5f86c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:41:35 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:41:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:41:38 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 18:58:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 18:58:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 18:58:32 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:58:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b67fbc3e5b36bd6602f2bfe0ee3e651234b80d90fadf2cf999749df2b40b27`  
		Last Modified: Thu, 23 Jul 2020 19:50:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a970e681d343ba286f519cb4ec238e076b07a7cfec4987e63d7d745347e60bd6`  
		Last Modified: Thu, 23 Jul 2020 19:50:06 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ed0f529cad4a8db22d58adc6c46b334cc83b696c99b3c671d5f803be00012`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc504f49399ad2198c7515cd1dc3438ecea31852f6f74ae3d66382469df7be0d`  
		Last Modified: Thu, 23 Jul 2020 19:51:00 GMT  
		Size: 455.8 MB (455846002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3d470189184407166c665554c86a97eeb245bcab47d55ea4e4c7396abc22b`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8586d73bdd27bddbb9c0c0265f41c60c1f8881b7909439400255e30e8d346a74`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008d6bf82ea1808f76b8569f83138d86a650a5ac78eafbffc32ff1c077a00e1`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:b97692594e0f23c58d1859d12e9515c8098f48c1a9ad6d17a50b1459f24da483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765492418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec7e890456c17b703dd39619addc9083928532e1b338551d13fca1f6ecf5b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:58:40 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:58:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:58:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 19:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:16:37 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:16:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bdae619d05db985c39b6ad49966019e7d3c53af0634697ce48984c62f28fa0`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4632cb3564f900163ab50d3acff20af90b8b27ae2495c91cf10fa2e0b02a2d8a`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3cd801f45fc0b7c8549109691f233c31a5ef9f2584899b59149e815e4cd6ec`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b03a831dc89ff2b94de9869ffafb4bd0f8d6d0534e777e4a6b924460c4971`  
		Last Modified: Thu, 23 Jul 2020 19:52:09 GMT  
		Size: 455.3 MB (455292150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa03bd57a8e83a36089fd27aec8731143f1fdfbfd35a6ea556a6c05ba3cf17`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166dd50f9c2e72c7dc4dc8772f70619d493b54a5e6e94ba20cfc66b090216a1`  
		Last Modified: Thu, 23 Jul 2020 19:51:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09663ebe0bc752ca2a2dbf19987d0d1eec4d0ed3c1355da55c27fca8d4b1066`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a8c621c7837356a751efad96caeb95f7611a19fa242573be440fadddadc70d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:3.6-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:b97692594e0f23c58d1859d12e9515c8098f48c1a9ad6d17a50b1459f24da483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765492418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec7e890456c17b703dd39619addc9083928532e1b338551d13fca1f6ecf5b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:58:40 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:58:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:58:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 19:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:16:37 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:16:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bdae619d05db985c39b6ad49966019e7d3c53af0634697ce48984c62f28fa0`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4632cb3564f900163ab50d3acff20af90b8b27ae2495c91cf10fa2e0b02a2d8a`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3cd801f45fc0b7c8549109691f233c31a5ef9f2584899b59149e815e4cd6ec`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b03a831dc89ff2b94de9869ffafb4bd0f8d6d0534e777e4a6b924460c4971`  
		Last Modified: Thu, 23 Jul 2020 19:52:09 GMT  
		Size: 455.3 MB (455292150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa03bd57a8e83a36089fd27aec8731143f1fdfbfd35a6ea556a6c05ba3cf17`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166dd50f9c2e72c7dc4dc8772f70619d493b54a5e6e94ba20cfc66b090216a1`  
		Last Modified: Thu, 23 Jul 2020 19:51:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09663ebe0bc752ca2a2dbf19987d0d1eec4d0ed3c1355da55c27fca8d4b1066`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:3856215bb112e8077ebb95b8847918cc83446cbdeab132daba9e319c91fafdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:3.6-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:7d4ab7df572f0d08a460d1fd24cc055a123f9cf6f8e1392fcb071aa3bb3d55a7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193316007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd386f37818d2ce37556036f90be88c80e05ad76e37608c26ebeb95648d5f86c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:41:35 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:41:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:41:38 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 18:58:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 18:58:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 18:58:32 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:58:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b67fbc3e5b36bd6602f2bfe0ee3e651234b80d90fadf2cf999749df2b40b27`  
		Last Modified: Thu, 23 Jul 2020 19:50:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a970e681d343ba286f519cb4ec238e076b07a7cfec4987e63d7d745347e60bd6`  
		Last Modified: Thu, 23 Jul 2020 19:50:06 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ed0f529cad4a8db22d58adc6c46b334cc83b696c99b3c671d5f803be00012`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc504f49399ad2198c7515cd1dc3438ecea31852f6f74ae3d66382469df7be0d`  
		Last Modified: Thu, 23 Jul 2020 19:51:00 GMT  
		Size: 455.8 MB (455846002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3d470189184407166c665554c86a97eeb245bcab47d55ea4e4c7396abc22b`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8586d73bdd27bddbb9c0c0265f41c60c1f8881b7909439400255e30e8d346a74`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008d6bf82ea1808f76b8569f83138d86a650a5ac78eafbffc32ff1c077a00e1`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-xenial`

```console
$ docker pull mongo@sha256:75c7759e6213d1e5b9575a7e2b47d53c15418957bc4d316a9a001d0f5ceeb5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6-xenial` - linux; amd64

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

### `mongo:3.6-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a6836de068e015e48898dd2a7f99139fd42153e9d521e077886a9f348eb4155d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155299204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a4b09162e7b7dde2a56907a2a0080f8d03b37bae2b2fd6390e3628837656ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:13:18 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:13:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:23 GMT
ENV MONGO_MAJOR=3.6
# Thu, 23 Jul 2020 18:44:54 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:45:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:45:54 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:46:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:46:08 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:46:09 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:46:11 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:46:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49fdddd7a4914963d409db49a451fab9f30114008fd6b3ab0a51483037fbd6c`  
		Last Modified: Mon, 06 Jul 2020 22:18:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1b7f0f3995be98399c02ad4abb2a3c35046c968c1e1b8219eaa8348a697af0`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f7d29c745886e2285d8c042322d2d2cd0b84a04ae5771f21ca1450383769c8`  
		Last Modified: Thu, 23 Jul 2020 18:49:02 GMT  
		Size: 111.6 MB (111589719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51adc290322c881bbe789cdc57dc04f174af859323617dd0c751f885853fa3c`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4216d9ee2bf67337acbb8059de2e7063f42e79bfdbcc73c28b05e25daca026f7`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:5c505f940177ca5cce5e4ae91ea8a755d94bd15f9df9ad0bbbdb9d0bbeecf2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:3-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:7d4ab7df572f0d08a460d1fd24cc055a123f9cf6f8e1392fcb071aa3bb3d55a7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193316007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd386f37818d2ce37556036f90be88c80e05ad76e37608c26ebeb95648d5f86c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:41:35 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:41:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:41:38 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 18:58:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 18:58:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 18:58:32 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:58:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b67fbc3e5b36bd6602f2bfe0ee3e651234b80d90fadf2cf999749df2b40b27`  
		Last Modified: Thu, 23 Jul 2020 19:50:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a970e681d343ba286f519cb4ec238e076b07a7cfec4987e63d7d745347e60bd6`  
		Last Modified: Thu, 23 Jul 2020 19:50:06 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ed0f529cad4a8db22d58adc6c46b334cc83b696c99b3c671d5f803be00012`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc504f49399ad2198c7515cd1dc3438ecea31852f6f74ae3d66382469df7be0d`  
		Last Modified: Thu, 23 Jul 2020 19:51:00 GMT  
		Size: 455.8 MB (455846002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3d470189184407166c665554c86a97eeb245bcab47d55ea4e4c7396abc22b`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8586d73bdd27bddbb9c0c0265f41c60c1f8881b7909439400255e30e8d346a74`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008d6bf82ea1808f76b8569f83138d86a650a5ac78eafbffc32ff1c077a00e1`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:b97692594e0f23c58d1859d12e9515c8098f48c1a9ad6d17a50b1459f24da483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765492418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec7e890456c17b703dd39619addc9083928532e1b338551d13fca1f6ecf5b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:58:40 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:58:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:58:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 19:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:16:37 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:16:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bdae619d05db985c39b6ad49966019e7d3c53af0634697ce48984c62f28fa0`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4632cb3564f900163ab50d3acff20af90b8b27ae2495c91cf10fa2e0b02a2d8a`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3cd801f45fc0b7c8549109691f233c31a5ef9f2584899b59149e815e4cd6ec`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b03a831dc89ff2b94de9869ffafb4bd0f8d6d0534e777e4a6b924460c4971`  
		Last Modified: Thu, 23 Jul 2020 19:52:09 GMT  
		Size: 455.3 MB (455292150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa03bd57a8e83a36089fd27aec8731143f1fdfbfd35a6ea556a6c05ba3cf17`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166dd50f9c2e72c7dc4dc8772f70619d493b54a5e6e94ba20cfc66b090216a1`  
		Last Modified: Thu, 23 Jul 2020 19:51:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09663ebe0bc752ca2a2dbf19987d0d1eec4d0ed3c1355da55c27fca8d4b1066`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a8c621c7837356a751efad96caeb95f7611a19fa242573be440fadddadc70d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:3-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:b97692594e0f23c58d1859d12e9515c8098f48c1a9ad6d17a50b1459f24da483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765492418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec7e890456c17b703dd39619addc9083928532e1b338551d13fca1f6ecf5b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:58:40 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:58:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:58:42 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 19:16:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:16:37 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:16:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bdae619d05db985c39b6ad49966019e7d3c53af0634697ce48984c62f28fa0`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4632cb3564f900163ab50d3acff20af90b8b27ae2495c91cf10fa2e0b02a2d8a`  
		Last Modified: Thu, 23 Jul 2020 19:51:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3cd801f45fc0b7c8549109691f233c31a5ef9f2584899b59149e815e4cd6ec`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b03a831dc89ff2b94de9869ffafb4bd0f8d6d0534e777e4a6b924460c4971`  
		Last Modified: Thu, 23 Jul 2020 19:52:09 GMT  
		Size: 455.3 MB (455292150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aa03bd57a8e83a36089fd27aec8731143f1fdfbfd35a6ea556a6c05ba3cf17`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166dd50f9c2e72c7dc4dc8772f70619d493b54a5e6e94ba20cfc66b090216a1`  
		Last Modified: Thu, 23 Jul 2020 19:51:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09663ebe0bc752ca2a2dbf19987d0d1eec4d0ed3c1355da55c27fca8d4b1066`  
		Last Modified: Thu, 23 Jul 2020 19:51:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:3856215bb112e8077ebb95b8847918cc83446cbdeab132daba9e319c91fafdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:7d4ab7df572f0d08a460d1fd24cc055a123f9cf6f8e1392fcb071aa3bb3d55a7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193316007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd386f37818d2ce37556036f90be88c80e05ad76e37608c26ebeb95648d5f86c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 18:41:35 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:41:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Thu, 23 Jul 2020 18:41:38 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Thu, 23 Jul 2020 18:58:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 18:58:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 18:58:32 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:58:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b67fbc3e5b36bd6602f2bfe0ee3e651234b80d90fadf2cf999749df2b40b27`  
		Last Modified: Thu, 23 Jul 2020 19:50:07 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a970e681d343ba286f519cb4ec238e076b07a7cfec4987e63d7d745347e60bd6`  
		Last Modified: Thu, 23 Jul 2020 19:50:06 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39ed0f529cad4a8db22d58adc6c46b334cc83b696c99b3c671d5f803be00012`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc504f49399ad2198c7515cd1dc3438ecea31852f6f74ae3d66382469df7be0d`  
		Last Modified: Thu, 23 Jul 2020 19:51:00 GMT  
		Size: 455.8 MB (455846002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae3d470189184407166c665554c86a97eeb245bcab47d55ea4e4c7396abc22b`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8586d73bdd27bddbb9c0c0265f41c60c1f8881b7909439400255e30e8d346a74`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008d6bf82ea1808f76b8569f83138d86a650a5ac78eafbffc32ff1c077a00e1`  
		Last Modified: Thu, 23 Jul 2020 19:50:04 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-xenial`

```console
$ docker pull mongo@sha256:75c7759e6213d1e5b9575a7e2b47d53c15418957bc4d316a9a001d0f5ceeb5c5
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
$ docker pull mongo@sha256:a6836de068e015e48898dd2a7f99139fd42153e9d521e077886a9f348eb4155d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155299204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a4b09162e7b7dde2a56907a2a0080f8d03b37bae2b2fd6390e3628837656ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:13:18 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:13:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:13:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:13:23 GMT
ENV MONGO_MAJOR=3.6
# Thu, 23 Jul 2020 18:44:54 GMT
ENV MONGO_VERSION=3.6.19
# Thu, 23 Jul 2020 18:45:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:45:54 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:46:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:46:08 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:46:09 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:46:11 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:46:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49fdddd7a4914963d409db49a451fab9f30114008fd6b3ab0a51483037fbd6c`  
		Last Modified: Mon, 06 Jul 2020 22:18:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1b7f0f3995be98399c02ad4abb2a3c35046c968c1e1b8219eaa8348a697af0`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f7d29c745886e2285d8c042322d2d2cd0b84a04ae5771f21ca1450383769c8`  
		Last Modified: Thu, 23 Jul 2020 18:49:02 GMT  
		Size: 111.6 MB (111589719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51adc290322c881bbe789cdc57dc04f174af859323617dd0c751f885853fa3c`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4216d9ee2bf67337acbb8059de2e7063f42e79bfdbcc73c28b05e25daca026f7`  
		Last Modified: Thu, 23 Jul 2020 18:48:29 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4`

```console
$ docker pull mongo@sha256:41f8e979f23624d1da534fee1b1e5c8d734173e18c510c1ababd375bba585534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4` - linux; amd64

```console
$ docker pull mongo@sha256:1c2243a5e21884ffa532ca9d20c221b170d7b40774c235619f98e2f6eaec520a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164661608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee5b549543c004a3498f23961d4738978409070141182195f2305d4aeac452c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:28:41 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 16:28:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 16:28:44 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:03 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:03 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:03 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af4dac7d70ea6794e7f6f0099cf3efc142c887488b3f6509eb872a45d2019f`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3823edc3c66e56ba812abc32fc96b4c10dc01cb2a3db7396916f639308c6662c`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbddf980229c3970fd52f08bfdc828b86e8dea8a9d526867c914f41099ab9df0`  
		Last Modified: Fri, 24 Jul 2020 16:30:56 GMT  
		Size: 129.1 MB (129122186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b1b60b739655778edd0020061c2381f1b2727657aa7d029b5e9e2a8a5a94d`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4592ef90c0ade4aaeac77b7c6dc9fd19234e2c0fdbbdd0cc8fd9e08870765120`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ff751a2fb9620cf8c8365e63d4e04b469246ca11d3fd3c778cde03a48f2006aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154674414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb889e5df20c6183f51f33be954ff870118609f845487614c8386f611946c6eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:15:56 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Mon, 06 Jul 2020 22:15:58 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:01 GMT
ENV MONGO_MAJOR=4.2
# Mon, 06 Jul 2020 22:16:02 GMT
ENV MONGO_VERSION=4.2.8
# Mon, 06 Jul 2020 22:16:04 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:16:29 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:16:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:16:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:16:34 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:16:36 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:16:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da8dd3b9fe4a2caac5977b8fd0ee6db66375a71cbb02c62717932c320f2343`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da5789bf40ba9ce0f4fa625e5d6e3a0736dc3e2d98c210c4f38e4285bc287c0`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0f9c45625791804dba83db5be92e028c9fec1682eb0030f8dfadabc454f49`  
		Last Modified: Mon, 06 Jul 2020 22:19:35 GMT  
		Size: 122.9 MB (122900108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d04d449a2731ebdc8507f7fb40a361de38d09987064ac93f8d039c295a2717`  
		Last Modified: Mon, 06 Jul 2020 22:19:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e28a037deb6b57194eb44b2769d3fb253fad9a2385b3b5a457b89c137a1376`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; s390x

```console
$ docker pull mongo@sha256:5db5812120b93c55c30b1b8626d7282704a6257d9679620b089cece050dfc3ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160602549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b37e732dec18de7fb04cbd6aeb6fc1fdf94f48de0e6725a7b9a29ae25dc0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:43:46 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 15:43:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 15:43:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:07 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:12 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:12 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:12 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ee891f925f24ddc2e8ccf8702934c12f13c780740bf68f160f4e5c5fe2ae`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a811584177c153f52f80ad54cea747d45227e567aa751413e4b6f45b93c31`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09fc4e97d3b4ad9658f9148e7b5a9141b09c97405b347246e532e78d41654c`  
		Last Modified: Fri, 24 Jul 2020 15:45:22 GMT  
		Size: 126.7 MB (126738049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0f29fcd01f15d95c9e432a029579555b523f7d62bc53c23df060c2e005c54`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a235bd7958c88d38f7f3c3886c775a56e1f018884bf8bd31334822677e18654`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 3.9 KB (3949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0`

```console
$ docker pull mongo@sha256:0c0c2069c3e5fe04f1d2fca022fe878830078fe979e83988d09180b9b458057b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.0` - linux; amd64

```console
$ docker pull mongo@sha256:c2de4a2e8316bc0aaafad1da54b5f6faa2a32160231a91972c0b6f9496781ea0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153874182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e76cad380fadd6db1bb87e326e2a8c5086b30a67dcf842c7b6914ef5ea26ee2`
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
# Fri, 24 Jul 2020 16:27:49 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 24 Jul 2020 16:27:49 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:27:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:27:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_MAJOR=4.0
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_VERSION=4.0.19
# Fri, 24 Jul 2020 16:27:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:28:09 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:28:10 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:28:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:28:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:28:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:28:10 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:28:10 GMT
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
	-	`sha256:0f5598a0c7768fed1770004986d0c7f6e002dacb17086cba6bf5410e534856ef`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d00ccb73233b02ddd7dfd9099e7b5780e79a81a5a1b4f01f60a841ed533f5`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a0168ae52b5841a1fcab5d31192356f2b0e358ee1003700a9960a98d4a1103`  
		Last Modified: Fri, 24 Jul 2020 16:30:34 GMT  
		Size: 105.3 MB (105254575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db33c3d00ce7bbec56266680195c90a4f9838521443b249bc0caeed8db43499`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e69d31d6c21283026ae432acda5b14772768571bfef64a964316d01e5e632e8`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 4.0 KB (3951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:16079db1a7e68e1c3955070bbf8f20d9b3b268c956a21d41021420d418ea671d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143394722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb86d7bf1c02a513b0095132bfcd2e85b5c2fbb084d759bb296c460f0555d152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:14:06 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Mon, 06 Jul 2020 22:14:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:14:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:14:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:14:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:14:12 GMT
ENV MONGO_MAJOR=4.0
# Mon, 06 Jul 2020 22:14:12 GMT
ENV MONGO_VERSION=4.0.19
# Mon, 06 Jul 2020 22:14:14 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:14:45 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:14:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:14:49 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:14:50 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:14:51 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:14:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5eff7df6c71240b2f470a5a886974c16d57a5e934ddf34ae50267bd5599417d`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1846d95b9b2770df63ad6b95afbcd8595f288b1c4112fe68ed47423e99753418`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af29b9b6f289c9bd0ff99ca9470caaad22c1a5bda290ec22974949ab4964e83`  
		Last Modified: Mon, 06 Jul 2020 22:19:03 GMT  
		Size: 99.7 MB (99685806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734351f572097c2cdb6ba9762444109b7276b9537b49cd2df21c693e6dfe688f`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9253ea69b2439224eb067f3addbecec06e9dd8c90e78bac27b6cf6c7276fa`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:23698c407a77c06d14bde74d6557c3c6dca3525f9b903d748f8e51b438f954ee
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5824206468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f628f6b43c8f15b85215eeb9841238bef4556a6e57e498803703039f4d1364f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:40:54 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:40:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:40:56 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 16:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 16:56:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 16:56:02 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 16:56:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8406541a4f2ce3b42db64d1f4a685a2f7a335fffe71b0c1604f08b466dc5c2`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a2bb41fe37245d15ab21953d4a2124b7dbac3d039f262e76b5ed22168ea1dc`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1406c6451134a125a8cf59e6812356d471c617b6164b61ae39ca64a03e663955`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14ce8b04817b4f38be92427ce91437f178a236de4c913cddad90f08508ddfbe`  
		Last Modified: Wed, 15 Jul 2020 18:24:58 GMT  
		Size: 86.7 MB (86736322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600a3eaece30200a2be6b0132fa86547fc1731b713835d6c1032deee9c862dd6`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a9d13242a7794806feecf11793150b022d390892dca1ed84072652d0a5a53d`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5baf0714092be1430e9f70d81d7e94bd412f260a7eb69e68abc5632c926bc5`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:a4a2b2946a3002f20684cd4473552c2d788ef1dee4cff455fcc383128c836231
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396242206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63f538673e63c4eebb9eec24c4a036b1104441dcfeb1a84b81e6b93791dce98`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:56:12 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:56:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:56:14 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 17:10:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:10:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:10:51 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:10:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27746377535a38f2e0a38f0c8375696bcccb60af6c7090f2e4a269c08501c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24230745cd261e2ba4fd3403e82609d955f11c86baff174be3da8525e7fefa3c`  
		Last Modified: Wed, 15 Jul 2020 18:25:15 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2b631267f8d7e3b1c8754b11354eeeea6b33cb75497489aa460c904930e8de`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3e2d8409e0965e18dec4d1d8a6bc834676c5c3bf24ac62dcd8c654a14cf4c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:32 GMT  
		Size: 86.0 MB (86041977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecab549a35d8e116f36001ec0643a27fac1edc6927b4e9820c57d378d49decc`  
		Last Modified: Wed, 15 Jul 2020 18:25:14 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e758ee80ec4d61e187f98a3e6ad736ea7151cd46d59d597ab5ab20a5470a76`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5739a808c5ac3970af764d8ea1cb16084243dd665e4007138c20a54a9d39a1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19`

```console
$ docker pull mongo@sha256:0c0c2069c3e5fe04f1d2fca022fe878830078fe979e83988d09180b9b458057b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.0.19` - linux; amd64

```console
$ docker pull mongo@sha256:c2de4a2e8316bc0aaafad1da54b5f6faa2a32160231a91972c0b6f9496781ea0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153874182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e76cad380fadd6db1bb87e326e2a8c5086b30a67dcf842c7b6914ef5ea26ee2`
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
# Fri, 24 Jul 2020 16:27:49 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 24 Jul 2020 16:27:49 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:27:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:27:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_MAJOR=4.0
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_VERSION=4.0.19
# Fri, 24 Jul 2020 16:27:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:28:09 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:28:10 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:28:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:28:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:28:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:28:10 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:28:10 GMT
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
	-	`sha256:0f5598a0c7768fed1770004986d0c7f6e002dacb17086cba6bf5410e534856ef`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d00ccb73233b02ddd7dfd9099e7b5780e79a81a5a1b4f01f60a841ed533f5`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a0168ae52b5841a1fcab5d31192356f2b0e358ee1003700a9960a98d4a1103`  
		Last Modified: Fri, 24 Jul 2020 16:30:34 GMT  
		Size: 105.3 MB (105254575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db33c3d00ce7bbec56266680195c90a4f9838521443b249bc0caeed8db43499`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e69d31d6c21283026ae432acda5b14772768571bfef64a964316d01e5e632e8`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 4.0 KB (3951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:16079db1a7e68e1c3955070bbf8f20d9b3b268c956a21d41021420d418ea671d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143394722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb86d7bf1c02a513b0095132bfcd2e85b5c2fbb084d759bb296c460f0555d152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:14:06 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Mon, 06 Jul 2020 22:14:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:14:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:14:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:14:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:14:12 GMT
ENV MONGO_MAJOR=4.0
# Mon, 06 Jul 2020 22:14:12 GMT
ENV MONGO_VERSION=4.0.19
# Mon, 06 Jul 2020 22:14:14 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:14:45 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:14:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:14:49 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:14:50 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:14:51 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:14:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5eff7df6c71240b2f470a5a886974c16d57a5e934ddf34ae50267bd5599417d`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1846d95b9b2770df63ad6b95afbcd8595f288b1c4112fe68ed47423e99753418`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af29b9b6f289c9bd0ff99ca9470caaad22c1a5bda290ec22974949ab4964e83`  
		Last Modified: Mon, 06 Jul 2020 22:19:03 GMT  
		Size: 99.7 MB (99685806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734351f572097c2cdb6ba9762444109b7276b9537b49cd2df21c693e6dfe688f`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9253ea69b2439224eb067f3addbecec06e9dd8c90e78bac27b6cf6c7276fa`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:23698c407a77c06d14bde74d6557c3c6dca3525f9b903d748f8e51b438f954ee
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5824206468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f628f6b43c8f15b85215eeb9841238bef4556a6e57e498803703039f4d1364f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:40:54 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:40:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:40:56 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 16:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 16:56:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 16:56:02 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 16:56:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8406541a4f2ce3b42db64d1f4a685a2f7a335fffe71b0c1604f08b466dc5c2`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a2bb41fe37245d15ab21953d4a2124b7dbac3d039f262e76b5ed22168ea1dc`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1406c6451134a125a8cf59e6812356d471c617b6164b61ae39ca64a03e663955`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14ce8b04817b4f38be92427ce91437f178a236de4c913cddad90f08508ddfbe`  
		Last Modified: Wed, 15 Jul 2020 18:24:58 GMT  
		Size: 86.7 MB (86736322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600a3eaece30200a2be6b0132fa86547fc1731b713835d6c1032deee9c862dd6`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a9d13242a7794806feecf11793150b022d390892dca1ed84072652d0a5a53d`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5baf0714092be1430e9f70d81d7e94bd412f260a7eb69e68abc5632c926bc5`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:a4a2b2946a3002f20684cd4473552c2d788ef1dee4cff455fcc383128c836231
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396242206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63f538673e63c4eebb9eec24c4a036b1104441dcfeb1a84b81e6b93791dce98`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:56:12 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:56:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:56:14 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 17:10:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:10:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:10:51 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:10:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27746377535a38f2e0a38f0c8375696bcccb60af6c7090f2e4a269c08501c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24230745cd261e2ba4fd3403e82609d955f11c86baff174be3da8525e7fefa3c`  
		Last Modified: Wed, 15 Jul 2020 18:25:15 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2b631267f8d7e3b1c8754b11354eeeea6b33cb75497489aa460c904930e8de`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3e2d8409e0965e18dec4d1d8a6bc834676c5c3bf24ac62dcd8c654a14cf4c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:32 GMT  
		Size: 86.0 MB (86041977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecab549a35d8e116f36001ec0643a27fac1edc6927b4e9820c57d378d49decc`  
		Last Modified: Wed, 15 Jul 2020 18:25:14 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e758ee80ec4d61e187f98a3e6ad736ea7151cd46d59d597ab5ab20a5470a76`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5739a808c5ac3970af764d8ea1cb16084243dd665e4007138c20a54a9d39a1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19-windowsservercore`

```console
$ docker pull mongo@sha256:55d7c01fc893360912aefd13027fa4a8e4f155bb3679b167128ee82690046b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.0.19-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:23698c407a77c06d14bde74d6557c3c6dca3525f9b903d748f8e51b438f954ee
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5824206468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f628f6b43c8f15b85215eeb9841238bef4556a6e57e498803703039f4d1364f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:40:54 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:40:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:40:56 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 16:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 16:56:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 16:56:02 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 16:56:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8406541a4f2ce3b42db64d1f4a685a2f7a335fffe71b0c1604f08b466dc5c2`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a2bb41fe37245d15ab21953d4a2124b7dbac3d039f262e76b5ed22168ea1dc`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1406c6451134a125a8cf59e6812356d471c617b6164b61ae39ca64a03e663955`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14ce8b04817b4f38be92427ce91437f178a236de4c913cddad90f08508ddfbe`  
		Last Modified: Wed, 15 Jul 2020 18:24:58 GMT  
		Size: 86.7 MB (86736322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600a3eaece30200a2be6b0132fa86547fc1731b713835d6c1032deee9c862dd6`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a9d13242a7794806feecf11793150b022d390892dca1ed84072652d0a5a53d`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5baf0714092be1430e9f70d81d7e94bd412f260a7eb69e68abc5632c926bc5`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:a4a2b2946a3002f20684cd4473552c2d788ef1dee4cff455fcc383128c836231
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396242206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63f538673e63c4eebb9eec24c4a036b1104441dcfeb1a84b81e6b93791dce98`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:56:12 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:56:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:56:14 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 17:10:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:10:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:10:51 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:10:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27746377535a38f2e0a38f0c8375696bcccb60af6c7090f2e4a269c08501c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24230745cd261e2ba4fd3403e82609d955f11c86baff174be3da8525e7fefa3c`  
		Last Modified: Wed, 15 Jul 2020 18:25:15 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2b631267f8d7e3b1c8754b11354eeeea6b33cb75497489aa460c904930e8de`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3e2d8409e0965e18dec4d1d8a6bc834676c5c3bf24ac62dcd8c654a14cf4c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:32 GMT  
		Size: 86.0 MB (86041977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecab549a35d8e116f36001ec0643a27fac1edc6927b4e9820c57d378d49decc`  
		Last Modified: Wed, 15 Jul 2020 18:25:14 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e758ee80ec4d61e187f98a3e6ad736ea7151cd46d59d597ab5ab20a5470a76`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5739a808c5ac3970af764d8ea1cb16084243dd665e4007138c20a54a9d39a1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19-windowsservercore-1809`

```console
$ docker pull mongo@sha256:0822ef2398a4626c0e25a4568cbb268ddfc331186b9c63cb6bf653750b13df51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.0.19-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:a4a2b2946a3002f20684cd4473552c2d788ef1dee4cff455fcc383128c836231
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396242206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63f538673e63c4eebb9eec24c4a036b1104441dcfeb1a84b81e6b93791dce98`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:56:12 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:56:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:56:14 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 17:10:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:10:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:10:51 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:10:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27746377535a38f2e0a38f0c8375696bcccb60af6c7090f2e4a269c08501c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24230745cd261e2ba4fd3403e82609d955f11c86baff174be3da8525e7fefa3c`  
		Last Modified: Wed, 15 Jul 2020 18:25:15 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2b631267f8d7e3b1c8754b11354eeeea6b33cb75497489aa460c904930e8de`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3e2d8409e0965e18dec4d1d8a6bc834676c5c3bf24ac62dcd8c654a14cf4c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:32 GMT  
		Size: 86.0 MB (86041977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecab549a35d8e116f36001ec0643a27fac1edc6927b4e9820c57d378d49decc`  
		Last Modified: Wed, 15 Jul 2020 18:25:14 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e758ee80ec4d61e187f98a3e6ad736ea7151cd46d59d597ab5ab20a5470a76`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5739a808c5ac3970af764d8ea1cb16084243dd665e4007138c20a54a9d39a1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:e138459a11cceb79f8e8c2d5511e6fd0b79547f43509b377df939f5a34586c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:4.0.19-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:23698c407a77c06d14bde74d6557c3c6dca3525f9b903d748f8e51b438f954ee
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5824206468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f628f6b43c8f15b85215eeb9841238bef4556a6e57e498803703039f4d1364f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:40:54 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:40:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:40:56 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 16:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 16:56:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 16:56:02 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 16:56:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8406541a4f2ce3b42db64d1f4a685a2f7a335fffe71b0c1604f08b466dc5c2`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a2bb41fe37245d15ab21953d4a2124b7dbac3d039f262e76b5ed22168ea1dc`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1406c6451134a125a8cf59e6812356d471c617b6164b61ae39ca64a03e663955`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14ce8b04817b4f38be92427ce91437f178a236de4c913cddad90f08508ddfbe`  
		Last Modified: Wed, 15 Jul 2020 18:24:58 GMT  
		Size: 86.7 MB (86736322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600a3eaece30200a2be6b0132fa86547fc1731b713835d6c1032deee9c862dd6`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a9d13242a7794806feecf11793150b022d390892dca1ed84072652d0a5a53d`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5baf0714092be1430e9f70d81d7e94bd412f260a7eb69e68abc5632c926bc5`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19-xenial`

```console
$ docker pull mongo@sha256:34c022273c7fb97f20cf95bf901866e919dff8d1da6936130f1ceafd33635e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0.19-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:c2de4a2e8316bc0aaafad1da54b5f6faa2a32160231a91972c0b6f9496781ea0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153874182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e76cad380fadd6db1bb87e326e2a8c5086b30a67dcf842c7b6914ef5ea26ee2`
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
# Fri, 24 Jul 2020 16:27:49 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 24 Jul 2020 16:27:49 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:27:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:27:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_MAJOR=4.0
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_VERSION=4.0.19
# Fri, 24 Jul 2020 16:27:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:28:09 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:28:10 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:28:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:28:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:28:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:28:10 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:28:10 GMT
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
	-	`sha256:0f5598a0c7768fed1770004986d0c7f6e002dacb17086cba6bf5410e534856ef`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d00ccb73233b02ddd7dfd9099e7b5780e79a81a5a1b4f01f60a841ed533f5`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a0168ae52b5841a1fcab5d31192356f2b0e358ee1003700a9960a98d4a1103`  
		Last Modified: Fri, 24 Jul 2020 16:30:34 GMT  
		Size: 105.3 MB (105254575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db33c3d00ce7bbec56266680195c90a4f9838521443b249bc0caeed8db43499`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e69d31d6c21283026ae432acda5b14772768571bfef64a964316d01e5e632e8`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 4.0 KB (3951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:16079db1a7e68e1c3955070bbf8f20d9b3b268c956a21d41021420d418ea671d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143394722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb86d7bf1c02a513b0095132bfcd2e85b5c2fbb084d759bb296c460f0555d152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:14:06 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Mon, 06 Jul 2020 22:14:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:14:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:14:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:14:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:14:12 GMT
ENV MONGO_MAJOR=4.0
# Mon, 06 Jul 2020 22:14:12 GMT
ENV MONGO_VERSION=4.0.19
# Mon, 06 Jul 2020 22:14:14 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:14:45 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:14:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:14:49 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:14:50 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:14:51 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:14:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5eff7df6c71240b2f470a5a886974c16d57a5e934ddf34ae50267bd5599417d`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1846d95b9b2770df63ad6b95afbcd8595f288b1c4112fe68ed47423e99753418`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af29b9b6f289c9bd0ff99ca9470caaad22c1a5bda290ec22974949ab4964e83`  
		Last Modified: Mon, 06 Jul 2020 22:19:03 GMT  
		Size: 99.7 MB (99685806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734351f572097c2cdb6ba9762444109b7276b9537b49cd2df21c693e6dfe688f`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9253ea69b2439224eb067f3addbecec06e9dd8c90e78bac27b6cf6c7276fa`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore`

```console
$ docker pull mongo@sha256:55d7c01fc893360912aefd13027fa4a8e4f155bb3679b167128ee82690046b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.0-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:23698c407a77c06d14bde74d6557c3c6dca3525f9b903d748f8e51b438f954ee
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5824206468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f628f6b43c8f15b85215eeb9841238bef4556a6e57e498803703039f4d1364f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:40:54 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:40:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:40:56 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 16:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 16:56:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 16:56:02 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 16:56:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8406541a4f2ce3b42db64d1f4a685a2f7a335fffe71b0c1604f08b466dc5c2`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a2bb41fe37245d15ab21953d4a2124b7dbac3d039f262e76b5ed22168ea1dc`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1406c6451134a125a8cf59e6812356d471c617b6164b61ae39ca64a03e663955`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14ce8b04817b4f38be92427ce91437f178a236de4c913cddad90f08508ddfbe`  
		Last Modified: Wed, 15 Jul 2020 18:24:58 GMT  
		Size: 86.7 MB (86736322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600a3eaece30200a2be6b0132fa86547fc1731b713835d6c1032deee9c862dd6`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a9d13242a7794806feecf11793150b022d390892dca1ed84072652d0a5a53d`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5baf0714092be1430e9f70d81d7e94bd412f260a7eb69e68abc5632c926bc5`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:a4a2b2946a3002f20684cd4473552c2d788ef1dee4cff455fcc383128c836231
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396242206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63f538673e63c4eebb9eec24c4a036b1104441dcfeb1a84b81e6b93791dce98`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:56:12 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:56:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:56:14 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 17:10:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:10:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:10:51 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:10:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27746377535a38f2e0a38f0c8375696bcccb60af6c7090f2e4a269c08501c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24230745cd261e2ba4fd3403e82609d955f11c86baff174be3da8525e7fefa3c`  
		Last Modified: Wed, 15 Jul 2020 18:25:15 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2b631267f8d7e3b1c8754b11354eeeea6b33cb75497489aa460c904930e8de`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3e2d8409e0965e18dec4d1d8a6bc834676c5c3bf24ac62dcd8c654a14cf4c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:32 GMT  
		Size: 86.0 MB (86041977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecab549a35d8e116f36001ec0643a27fac1edc6927b4e9820c57d378d49decc`  
		Last Modified: Wed, 15 Jul 2020 18:25:14 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e758ee80ec4d61e187f98a3e6ad736ea7151cd46d59d597ab5ab20a5470a76`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5739a808c5ac3970af764d8ea1cb16084243dd665e4007138c20a54a9d39a1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore-1809`

```console
$ docker pull mongo@sha256:0822ef2398a4626c0e25a4568cbb268ddfc331186b9c63cb6bf653750b13df51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.0-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:a4a2b2946a3002f20684cd4473552c2d788ef1dee4cff455fcc383128c836231
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396242206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63f538673e63c4eebb9eec24c4a036b1104441dcfeb1a84b81e6b93791dce98`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:56:12 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:56:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:56:14 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 17:10:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:10:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:10:51 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:10:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27746377535a38f2e0a38f0c8375696bcccb60af6c7090f2e4a269c08501c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24230745cd261e2ba4fd3403e82609d955f11c86baff174be3da8525e7fefa3c`  
		Last Modified: Wed, 15 Jul 2020 18:25:15 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2b631267f8d7e3b1c8754b11354eeeea6b33cb75497489aa460c904930e8de`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3e2d8409e0965e18dec4d1d8a6bc834676c5c3bf24ac62dcd8c654a14cf4c7`  
		Last Modified: Wed, 15 Jul 2020 18:25:32 GMT  
		Size: 86.0 MB (86041977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecab549a35d8e116f36001ec0643a27fac1edc6927b4e9820c57d378d49decc`  
		Last Modified: Wed, 15 Jul 2020 18:25:14 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e758ee80ec4d61e187f98a3e6ad736ea7151cd46d59d597ab5ab20a5470a76`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5739a808c5ac3970af764d8ea1cb16084243dd665e4007138c20a54a9d39a1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:13 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:e138459a11cceb79f8e8c2d5511e6fd0b79547f43509b377df939f5a34586c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:4.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:23698c407a77c06d14bde74d6557c3c6dca3525f9b903d748f8e51b438f954ee
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5824206468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f628f6b43c8f15b85215eeb9841238bef4556a6e57e498803703039f4d1364f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:40:54 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 15 Jul 2020 16:40:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 15 Jul 2020 16:40:56 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 15 Jul 2020 16:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 16:56:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 16:56:02 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 16:56:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8406541a4f2ce3b42db64d1f4a685a2f7a335fffe71b0c1604f08b466dc5c2`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a2bb41fe37245d15ab21953d4a2124b7dbac3d039f262e76b5ed22168ea1dc`  
		Last Modified: Wed, 15 Jul 2020 18:24:40 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1406c6451134a125a8cf59e6812356d471c617b6164b61ae39ca64a03e663955`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14ce8b04817b4f38be92427ce91437f178a236de4c913cddad90f08508ddfbe`  
		Last Modified: Wed, 15 Jul 2020 18:24:58 GMT  
		Size: 86.7 MB (86736322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600a3eaece30200a2be6b0132fa86547fc1731b713835d6c1032deee9c862dd6`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a9d13242a7794806feecf11793150b022d390892dca1ed84072652d0a5a53d`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5baf0714092be1430e9f70d81d7e94bd412f260a7eb69e68abc5632c926bc5`  
		Last Modified: Wed, 15 Jul 2020 18:24:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-xenial`

```console
$ docker pull mongo@sha256:34c022273c7fb97f20cf95bf901866e919dff8d1da6936130f1ceafd33635e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:c2de4a2e8316bc0aaafad1da54b5f6faa2a32160231a91972c0b6f9496781ea0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153874182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e76cad380fadd6db1bb87e326e2a8c5086b30a67dcf842c7b6914ef5ea26ee2`
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
# Fri, 24 Jul 2020 16:27:49 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 24 Jul 2020 16:27:49 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:27:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:27:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_MAJOR=4.0
# Fri, 24 Jul 2020 16:27:50 GMT
ENV MONGO_VERSION=4.0.19
# Fri, 24 Jul 2020 16:27:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:28:09 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:28:10 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:28:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:28:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:28:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:28:10 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:28:10 GMT
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
	-	`sha256:0f5598a0c7768fed1770004986d0c7f6e002dacb17086cba6bf5410e534856ef`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d00ccb73233b02ddd7dfd9099e7b5780e79a81a5a1b4f01f60a841ed533f5`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a0168ae52b5841a1fcab5d31192356f2b0e358ee1003700a9960a98d4a1103`  
		Last Modified: Fri, 24 Jul 2020 16:30:34 GMT  
		Size: 105.3 MB (105254575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db33c3d00ce7bbec56266680195c90a4f9838521443b249bc0caeed8db43499`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e69d31d6c21283026ae432acda5b14772768571bfef64a964316d01e5e632e8`  
		Last Modified: Fri, 24 Jul 2020 16:30:18 GMT  
		Size: 4.0 KB (3951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:16079db1a7e68e1c3955070bbf8f20d9b3b268c956a21d41021420d418ea671d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143394722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb86d7bf1c02a513b0095132bfcd2e85b5c2fbb084d759bb296c460f0555d152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:06:25 GMT
ADD file:eacc4e3c71dca085a01eb1b781c8312350bcb2288a1f6ceeefb68d660b3215b5 in / 
# Mon, 06 Jul 2020 22:06:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:06:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:06:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:06:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:12:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:12:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:12:50 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:12:51 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:13:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:13:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:14:06 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Mon, 06 Jul 2020 22:14:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:14:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:14:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:14:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:14:12 GMT
ENV MONGO_MAJOR=4.0
# Mon, 06 Jul 2020 22:14:12 GMT
ENV MONGO_VERSION=4.0.19
# Mon, 06 Jul 2020 22:14:14 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:14:45 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:14:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:14:49 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:14:50 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:14:51 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:14:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ab489c2a6275c4f4b0c3ccbc0c397c7b4d1e3278136f158f0345707b88775ce`  
		Last Modified: Sat, 20 Jun 2020 00:25:22 GMT  
		Size: 40.0 MB (40035468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7a7bb5cc1bf1dc02973eb563c00d2491059923f17bdcc83b37d65a6015b74`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150055c00370319e479ec8c335cd23b2564e0546e6e50593f651a6311be5a83`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee51ca48c53d0f23ff69410d387087d1f50be8472db56cb051f280b80038ac7`  
		Last Modified: Mon, 06 Jul 2020 22:07:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24de82b2c5a19d2f7a7e7ce7d627fbf0070f0674ace725f0fbfe1f793bf8109a`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd459d6e72251ae322dda8d198235de3ed071b81a8332a6024f6aafbb6339fc`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 2.4 MB (2431917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e501977e32238fc13cab63f9b116cb2b006b70dd76c86228a7769b73fd80c0`  
		Last Modified: Mon, 06 Jul 2020 22:18:05 GMT  
		Size: 1.2 MB (1232095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e722a92087fc18361ee12e85b17e239d785cdd1553559797dfd0675cc0c879c9`  
		Last Modified: Mon, 06 Jul 2020 22:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5eff7df6c71240b2f470a5a886974c16d57a5e934ddf34ae50267bd5599417d`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1846d95b9b2770df63ad6b95afbcd8595f288b1c4112fe68ed47423e99753418`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af29b9b6f289c9bd0ff99ca9470caaad22c1a5bda290ec22974949ab4964e83`  
		Last Modified: Mon, 06 Jul 2020 22:19:03 GMT  
		Size: 99.7 MB (99685806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734351f572097c2cdb6ba9762444109b7276b9537b49cd2df21c693e6dfe688f`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9253ea69b2439224eb067f3addbecec06e9dd8c90e78bac27b6cf6c7276fa`  
		Last Modified: Mon, 06 Jul 2020 22:18:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2`

```console
$ docker pull mongo@sha256:41f8e979f23624d1da534fee1b1e5c8d734173e18c510c1ababd375bba585534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.2` - linux; amd64

```console
$ docker pull mongo@sha256:1c2243a5e21884ffa532ca9d20c221b170d7b40774c235619f98e2f6eaec520a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164661608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee5b549543c004a3498f23961d4738978409070141182195f2305d4aeac452c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:28:41 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 16:28:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 16:28:44 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:03 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:03 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:03 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af4dac7d70ea6794e7f6f0099cf3efc142c887488b3f6509eb872a45d2019f`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3823edc3c66e56ba812abc32fc96b4c10dc01cb2a3db7396916f639308c6662c`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbddf980229c3970fd52f08bfdc828b86e8dea8a9d526867c914f41099ab9df0`  
		Last Modified: Fri, 24 Jul 2020 16:30:56 GMT  
		Size: 129.1 MB (129122186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b1b60b739655778edd0020061c2381f1b2727657aa7d029b5e9e2a8a5a94d`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4592ef90c0ade4aaeac77b7c6dc9fd19234e2c0fdbbdd0cc8fd9e08870765120`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ff751a2fb9620cf8c8365e63d4e04b469246ca11d3fd3c778cde03a48f2006aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154674414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb889e5df20c6183f51f33be954ff870118609f845487614c8386f611946c6eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:15:56 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Mon, 06 Jul 2020 22:15:58 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:01 GMT
ENV MONGO_MAJOR=4.2
# Mon, 06 Jul 2020 22:16:02 GMT
ENV MONGO_VERSION=4.2.8
# Mon, 06 Jul 2020 22:16:04 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:16:29 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:16:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:16:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:16:34 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:16:36 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:16:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da8dd3b9fe4a2caac5977b8fd0ee6db66375a71cbb02c62717932c320f2343`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da5789bf40ba9ce0f4fa625e5d6e3a0736dc3e2d98c210c4f38e4285bc287c0`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0f9c45625791804dba83db5be92e028c9fec1682eb0030f8dfadabc454f49`  
		Last Modified: Mon, 06 Jul 2020 22:19:35 GMT  
		Size: 122.9 MB (122900108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d04d449a2731ebdc8507f7fb40a361de38d09987064ac93f8d039c295a2717`  
		Last Modified: Mon, 06 Jul 2020 22:19:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e28a037deb6b57194eb44b2769d3fb253fad9a2385b3b5a457b89c137a1376`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; s390x

```console
$ docker pull mongo@sha256:5db5812120b93c55c30b1b8626d7282704a6257d9679620b089cece050dfc3ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160602549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b37e732dec18de7fb04cbd6aeb6fc1fdf94f48de0e6725a7b9a29ae25dc0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:43:46 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 15:43:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 15:43:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:07 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:12 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:12 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:12 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ee891f925f24ddc2e8ccf8702934c12f13c780740bf68f160f4e5c5fe2ae`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a811584177c153f52f80ad54cea747d45227e567aa751413e4b6f45b93c31`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09fc4e97d3b4ad9658f9148e7b5a9141b09c97405b347246e532e78d41654c`  
		Last Modified: Fri, 24 Jul 2020 15:45:22 GMT  
		Size: 126.7 MB (126738049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0f29fcd01f15d95c9e432a029579555b523f7d62bc53c23df060c2e005c54`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a235bd7958c88d38f7f3c3886c775a56e1f018884bf8bd31334822677e18654`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 3.9 KB (3949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8`

```console
$ docker pull mongo@sha256:41f8e979f23624d1da534fee1b1e5c8d734173e18c510c1ababd375bba585534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.2.8` - linux; amd64

```console
$ docker pull mongo@sha256:1c2243a5e21884ffa532ca9d20c221b170d7b40774c235619f98e2f6eaec520a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164661608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee5b549543c004a3498f23961d4738978409070141182195f2305d4aeac452c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:28:41 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 16:28:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 16:28:44 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:03 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:03 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:03 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af4dac7d70ea6794e7f6f0099cf3efc142c887488b3f6509eb872a45d2019f`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3823edc3c66e56ba812abc32fc96b4c10dc01cb2a3db7396916f639308c6662c`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbddf980229c3970fd52f08bfdc828b86e8dea8a9d526867c914f41099ab9df0`  
		Last Modified: Fri, 24 Jul 2020 16:30:56 GMT  
		Size: 129.1 MB (129122186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b1b60b739655778edd0020061c2381f1b2727657aa7d029b5e9e2a8a5a94d`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4592ef90c0ade4aaeac77b7c6dc9fd19234e2c0fdbbdd0cc8fd9e08870765120`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ff751a2fb9620cf8c8365e63d4e04b469246ca11d3fd3c778cde03a48f2006aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154674414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb889e5df20c6183f51f33be954ff870118609f845487614c8386f611946c6eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:15:56 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Mon, 06 Jul 2020 22:15:58 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:01 GMT
ENV MONGO_MAJOR=4.2
# Mon, 06 Jul 2020 22:16:02 GMT
ENV MONGO_VERSION=4.2.8
# Mon, 06 Jul 2020 22:16:04 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:16:29 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:16:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:16:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:16:34 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:16:36 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:16:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da8dd3b9fe4a2caac5977b8fd0ee6db66375a71cbb02c62717932c320f2343`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da5789bf40ba9ce0f4fa625e5d6e3a0736dc3e2d98c210c4f38e4285bc287c0`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0f9c45625791804dba83db5be92e028c9fec1682eb0030f8dfadabc454f49`  
		Last Modified: Mon, 06 Jul 2020 22:19:35 GMT  
		Size: 122.9 MB (122900108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d04d449a2731ebdc8507f7fb40a361de38d09987064ac93f8d039c295a2717`  
		Last Modified: Mon, 06 Jul 2020 22:19:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e28a037deb6b57194eb44b2769d3fb253fad9a2385b3b5a457b89c137a1376`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8` - linux; s390x

```console
$ docker pull mongo@sha256:5db5812120b93c55c30b1b8626d7282704a6257d9679620b089cece050dfc3ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160602549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b37e732dec18de7fb04cbd6aeb6fc1fdf94f48de0e6725a7b9a29ae25dc0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:43:46 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 15:43:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 15:43:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:07 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:12 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:12 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:12 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ee891f925f24ddc2e8ccf8702934c12f13c780740bf68f160f4e5c5fe2ae`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a811584177c153f52f80ad54cea747d45227e567aa751413e4b6f45b93c31`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09fc4e97d3b4ad9658f9148e7b5a9141b09c97405b347246e532e78d41654c`  
		Last Modified: Fri, 24 Jul 2020 15:45:22 GMT  
		Size: 126.7 MB (126738049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0f29fcd01f15d95c9e432a029579555b523f7d62bc53c23df060c2e005c54`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a235bd7958c88d38f7f3c3886c775a56e1f018884bf8bd31334822677e18654`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 3.9 KB (3949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8-bionic`

```console
$ docker pull mongo@sha256:d5d4b6b5a8e19049338b966b55931fa5f24f21967cefdb4e61327bef69fb634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.2.8-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:1c2243a5e21884ffa532ca9d20c221b170d7b40774c235619f98e2f6eaec520a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164661608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee5b549543c004a3498f23961d4738978409070141182195f2305d4aeac452c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:28:41 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 16:28:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 16:28:44 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:03 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:03 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:03 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af4dac7d70ea6794e7f6f0099cf3efc142c887488b3f6509eb872a45d2019f`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3823edc3c66e56ba812abc32fc96b4c10dc01cb2a3db7396916f639308c6662c`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbddf980229c3970fd52f08bfdc828b86e8dea8a9d526867c914f41099ab9df0`  
		Last Modified: Fri, 24 Jul 2020 16:30:56 GMT  
		Size: 129.1 MB (129122186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b1b60b739655778edd0020061c2381f1b2727657aa7d029b5e9e2a8a5a94d`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4592ef90c0ade4aaeac77b7c6dc9fd19234e2c0fdbbdd0cc8fd9e08870765120`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ff751a2fb9620cf8c8365e63d4e04b469246ca11d3fd3c778cde03a48f2006aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154674414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb889e5df20c6183f51f33be954ff870118609f845487614c8386f611946c6eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:15:56 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Mon, 06 Jul 2020 22:15:58 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:01 GMT
ENV MONGO_MAJOR=4.2
# Mon, 06 Jul 2020 22:16:02 GMT
ENV MONGO_VERSION=4.2.8
# Mon, 06 Jul 2020 22:16:04 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:16:29 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:16:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:16:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:16:34 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:16:36 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:16:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da8dd3b9fe4a2caac5977b8fd0ee6db66375a71cbb02c62717932c320f2343`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da5789bf40ba9ce0f4fa625e5d6e3a0736dc3e2d98c210c4f38e4285bc287c0`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0f9c45625791804dba83db5be92e028c9fec1682eb0030f8dfadabc454f49`  
		Last Modified: Mon, 06 Jul 2020 22:19:35 GMT  
		Size: 122.9 MB (122900108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d04d449a2731ebdc8507f7fb40a361de38d09987064ac93f8d039c295a2717`  
		Last Modified: Mon, 06 Jul 2020 22:19:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e28a037deb6b57194eb44b2769d3fb253fad9a2385b3b5a457b89c137a1376`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:5db5812120b93c55c30b1b8626d7282704a6257d9679620b089cece050dfc3ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160602549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b37e732dec18de7fb04cbd6aeb6fc1fdf94f48de0e6725a7b9a29ae25dc0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:43:46 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 15:43:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 15:43:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:07 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:12 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:12 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:12 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ee891f925f24ddc2e8ccf8702934c12f13c780740bf68f160f4e5c5fe2ae`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a811584177c153f52f80ad54cea747d45227e567aa751413e4b6f45b93c31`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09fc4e97d3b4ad9658f9148e7b5a9141b09c97405b347246e532e78d41654c`  
		Last Modified: Fri, 24 Jul 2020 15:45:22 GMT  
		Size: 126.7 MB (126738049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0f29fcd01f15d95c9e432a029579555b523f7d62bc53c23df060c2e005c54`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a235bd7958c88d38f7f3c3886c775a56e1f018884bf8bd31334822677e18654`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 3.9 KB (3949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8-windowsservercore`

```console
$ docker pull mongo@sha256:ff58ef6f07de1f251dbccead1949f582e75519bfd18b82cd6dd03f46f53784e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.2.8-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8-windowsservercore-1809`

```console
$ docker pull mongo@sha256:8d7f9b3710dcd74d916c3f250672932aa3d646eacad6fe9c25a0734e416c9d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.2.8-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:f06909500296ef95416990ad20e3fc408027df1f49a882c7f75137f7dfb21862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:4.2.8-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-bionic`

```console
$ docker pull mongo@sha256:d5d4b6b5a8e19049338b966b55931fa5f24f21967cefdb4e61327bef69fb634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.2-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:1c2243a5e21884ffa532ca9d20c221b170d7b40774c235619f98e2f6eaec520a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164661608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee5b549543c004a3498f23961d4738978409070141182195f2305d4aeac452c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:28:41 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 16:28:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 16:28:44 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:03 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:03 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:03 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af4dac7d70ea6794e7f6f0099cf3efc142c887488b3f6509eb872a45d2019f`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3823edc3c66e56ba812abc32fc96b4c10dc01cb2a3db7396916f639308c6662c`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbddf980229c3970fd52f08bfdc828b86e8dea8a9d526867c914f41099ab9df0`  
		Last Modified: Fri, 24 Jul 2020 16:30:56 GMT  
		Size: 129.1 MB (129122186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b1b60b739655778edd0020061c2381f1b2727657aa7d029b5e9e2a8a5a94d`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4592ef90c0ade4aaeac77b7c6dc9fd19234e2c0fdbbdd0cc8fd9e08870765120`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ff751a2fb9620cf8c8365e63d4e04b469246ca11d3fd3c778cde03a48f2006aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154674414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb889e5df20c6183f51f33be954ff870118609f845487614c8386f611946c6eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:15:56 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Mon, 06 Jul 2020 22:15:58 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:01 GMT
ENV MONGO_MAJOR=4.2
# Mon, 06 Jul 2020 22:16:02 GMT
ENV MONGO_VERSION=4.2.8
# Mon, 06 Jul 2020 22:16:04 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:16:29 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:16:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:16:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:16:34 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:16:36 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:16:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da8dd3b9fe4a2caac5977b8fd0ee6db66375a71cbb02c62717932c320f2343`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da5789bf40ba9ce0f4fa625e5d6e3a0736dc3e2d98c210c4f38e4285bc287c0`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0f9c45625791804dba83db5be92e028c9fec1682eb0030f8dfadabc454f49`  
		Last Modified: Mon, 06 Jul 2020 22:19:35 GMT  
		Size: 122.9 MB (122900108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d04d449a2731ebdc8507f7fb40a361de38d09987064ac93f8d039c295a2717`  
		Last Modified: Mon, 06 Jul 2020 22:19:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e28a037deb6b57194eb44b2769d3fb253fad9a2385b3b5a457b89c137a1376`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:5db5812120b93c55c30b1b8626d7282704a6257d9679620b089cece050dfc3ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160602549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b37e732dec18de7fb04cbd6aeb6fc1fdf94f48de0e6725a7b9a29ae25dc0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:43:46 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 15:43:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 15:43:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:07 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:12 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:12 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:12 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ee891f925f24ddc2e8ccf8702934c12f13c780740bf68f160f4e5c5fe2ae`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a811584177c153f52f80ad54cea747d45227e567aa751413e4b6f45b93c31`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09fc4e97d3b4ad9658f9148e7b5a9141b09c97405b347246e532e78d41654c`  
		Last Modified: Fri, 24 Jul 2020 15:45:22 GMT  
		Size: 126.7 MB (126738049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0f29fcd01f15d95c9e432a029579555b523f7d62bc53c23df060c2e005c54`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a235bd7958c88d38f7f3c3886c775a56e1f018884bf8bd31334822677e18654`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 3.9 KB (3949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore`

```console
$ docker pull mongo@sha256:ff58ef6f07de1f251dbccead1949f582e75519bfd18b82cd6dd03f46f53784e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.2-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore-1809`

```console
$ docker pull mongo@sha256:8d7f9b3710dcd74d916c3f250672932aa3d646eacad6fe9c25a0734e416c9d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.2-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:f06909500296ef95416990ad20e3fc408027df1f49a882c7f75137f7dfb21862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:4.2-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc14`

```console
$ docker pull mongo@sha256:c393c09247bd3e9071e7ce46b211bb79e34660e480daa8702b06f05cb5b614c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.4.0-rc14` - linux; amd64

```console
$ docker pull mongo@sha256:bde690522196eb751b3c17689fa2e7b887f802b254518df50abaac9d82d9760c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177975003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c77712af1a38ff8f4cac7c28abb9787ff682cf389a107c58370780b69d36f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:29:13 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Jul 2020 16:29:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:29:15 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:29:15 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_MAJOR=testing
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Fri, 24 Jul 2020 16:29:16 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:40 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:40 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb942b17a59a8571f29488b50c40c51066e0efeac607b0bf0ac4100867d6fd3`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 6.3 KB (6251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2dae5231420c9acea900e9db4ad239422c3d80c23d91056980cfa09328b7ac`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb360f7104ab05ff0ed656a6a38f93c2d160d5bd667293780a0ebd6cb217029`  
		Last Modified: Fri, 24 Jul 2020 16:31:24 GMT  
		Size: 142.4 MB (142430756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05faea633d8b9266956c4d2a16aad66ef4f8dbc3b633290606f3ffb48e076968`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8546cbdb1cbcb75ad7cca67b243133c90007d5c6f1c36019a3538194ba1de34`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 4.0 KB (3951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc14` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b71539d673cad78259193407619c1ad22a50ff243f3916f93c5d5148ad9bc1cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167713824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb863a666bab8637029395a9356a3dd84606ecbc0f65aa80259f573d064a9490`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:16:53 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:16:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:16:56 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:16:57 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:58 GMT
ENV MONGO_MAJOR=testing
# Thu, 23 Jul 2020 18:46:45 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Thu, 23 Jul 2020 18:46:52 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:47:36 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:47:44 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:47:45 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:47:47 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:47:50 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:47:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c7dd9701ffc1428880bb0d6d480a9c5ed781b5a93786ddaf99a0e9fee5e5cf`  
		Last Modified: Mon, 06 Jul 2020 22:20:02 GMT  
		Size: 6.3 KB (6254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b64a1a43c684c5c8fb0b279ed8c7c4141ff239d79a1120ab3dfd300c44ba4`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a6906db4f2984ecfceded05cfbd9591acfd2d77617d178f499ff385bc6ba3`  
		Last Modified: Thu, 23 Jul 2020 18:49:55 GMT  
		Size: 135.9 MB (135934696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1364c9d6721b53b1bd8778cb0d0ac87c86ed89e9dd342561ba2929dd95da275`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f945cae44a06e4c6a1675372333e392585e86f506b67a2e7318916725bee112`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc14` - linux; s390x

```console
$ docker pull mongo@sha256:320e86de94f1766bc0b99968e01cc228a1c174d7ef03ca6fdea6b2beb79d19ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172898995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4556d6c47cee365c69938eff1c624edd885fccdf75221a14faeaa18799c1708a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:44:24 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Jul 2020 15:44:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:44:25 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:44:25 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:44:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:44:26 GMT
ENV MONGO_MAJOR=testing
# Fri, 24 Jul 2020 15:44:26 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Fri, 24 Jul 2020 15:44:26 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:46 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:52 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:52 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:52 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:53 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7846067e8c01b36594de6ff45d2d0009185a0a644f67e72d3f92d1b93632ee9e`  
		Last Modified: Fri, 24 Jul 2020 15:45:31 GMT  
		Size: 6.2 KB (6246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a2ff24811f96ec5c958284ebae49f0e4a05b93286c074721e96b9bec777827`  
		Last Modified: Fri, 24 Jul 2020 15:45:31 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e008bc650289579ec33129da28aec09626f0c279d9e50ad7f098f017ed49b3f1`  
		Last Modified: Fri, 24 Jul 2020 15:45:50 GMT  
		Size: 139.0 MB (139029683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fb3ee0131a773b21e3ecb0447a81b982bd346438608b31b807470e468b496c`  
		Last Modified: Fri, 24 Jul 2020 15:46:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885fab2cbb3ccf8839b04ab7a43fc58eb09741c03f40881c79b345aaba312863`  
		Last Modified: Fri, 24 Jul 2020 15:46:22 GMT  
		Size: 3.9 KB (3948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc14` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:172923a3c78e83de59a1e39e6db82e58a7133749ad9b41d320c03d257d3c44d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788364909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3ca42939f0b381c5792c06b47b048b23917e1da151bac43c13e9b86b478d7e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:17:03 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:17:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:17:05 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:30:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:30:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:30:53 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:30:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e03356e08c8f22ba6d71af8158646023fcc548e12f61c140007602c48873b3c`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d9c4688c8933a4e69cc3bd825ebab126557b6cefc7a7c0cde026d978442f8`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7686ce7eff68540ecbe87721a6c125c23c0ed14013f583241951500bad1b63c`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d2efade707503ce77b32f40675ffb6614e019fc90d911a2bb67b28f0e6715`  
		Last Modified: Thu, 23 Jul 2020 19:52:37 GMT  
		Size: 50.9 MB (50895014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22999ec35a51336544400b70143ef4695a2c45bef62861647214a3efa547d130`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a034beacfee6bc7401c5a99eb4ba13f78c0eb246f15ae1a8febf7ed2c6b4aa`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec07982643704a5e6385e3096821f7884d27d1a98a04c022c5a94defd2c10d1`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc14` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:aee6a672b5020ea8847a205151b2d825888c9437786b02a01a04b77539042833
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2722607823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6314d3e4e52f15d59bb1d397b078528323ca40e0104a13f54bce7738d8e411`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:31:04 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:31:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:31:07 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:49:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:49:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:49:07 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd666845ca3bdcc15c24652e0ff79e818b4d354ed8d9f00a9b78c0a69fb0dea1`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23643aa0c2818301a47e42fedeaa69d320141a602993824327ee39034d79d83`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ec84d6a917f6fc3d70328053e275180956b182e9c17814ab2ea3824d789b7`  
		Last Modified: Thu, 23 Jul 2020 19:52:48 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e99108a8f1ac902218296eabd2ca1661fa2c97d872ef52cf3b807e3146eda25`  
		Last Modified: Thu, 23 Jul 2020 19:53:33 GMT  
		Size: 412.4 MB (412407713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5c2cf8ea61e8374ec34fc6fa6fa5a44754721cec2905155ca79d847927087c`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455ff26c7051f08d062c946fa3968c4cc7aad659875c18e725b9b46a8508376e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111fda336322ed7db23e968ca25ce17c9a022ed20ba8caf1e8c523d00087a3e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc14-bionic`

```console
$ docker pull mongo@sha256:539e92ee53f9bd4bb10e8d89367dc8c82c3bea026feaa3b2d535468864cc7ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.4.0-rc14-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:bde690522196eb751b3c17689fa2e7b887f802b254518df50abaac9d82d9760c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177975003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c77712af1a38ff8f4cac7c28abb9787ff682cf389a107c58370780b69d36f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:29:13 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Jul 2020 16:29:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:29:15 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:29:15 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_MAJOR=testing
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Fri, 24 Jul 2020 16:29:16 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:40 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:40 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb942b17a59a8571f29488b50c40c51066e0efeac607b0bf0ac4100867d6fd3`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 6.3 KB (6251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2dae5231420c9acea900e9db4ad239422c3d80c23d91056980cfa09328b7ac`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb360f7104ab05ff0ed656a6a38f93c2d160d5bd667293780a0ebd6cb217029`  
		Last Modified: Fri, 24 Jul 2020 16:31:24 GMT  
		Size: 142.4 MB (142430756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05faea633d8b9266956c4d2a16aad66ef4f8dbc3b633290606f3ffb48e076968`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8546cbdb1cbcb75ad7cca67b243133c90007d5c6f1c36019a3538194ba1de34`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 4.0 KB (3951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc14-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b71539d673cad78259193407619c1ad22a50ff243f3916f93c5d5148ad9bc1cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167713824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb863a666bab8637029395a9356a3dd84606ecbc0f65aa80259f573d064a9490`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:16:53 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:16:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:16:56 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:16:57 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:58 GMT
ENV MONGO_MAJOR=testing
# Thu, 23 Jul 2020 18:46:45 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Thu, 23 Jul 2020 18:46:52 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:47:36 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:47:44 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:47:45 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:47:47 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:47:50 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:47:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c7dd9701ffc1428880bb0d6d480a9c5ed781b5a93786ddaf99a0e9fee5e5cf`  
		Last Modified: Mon, 06 Jul 2020 22:20:02 GMT  
		Size: 6.3 KB (6254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b64a1a43c684c5c8fb0b279ed8c7c4141ff239d79a1120ab3dfd300c44ba4`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a6906db4f2984ecfceded05cfbd9591acfd2d77617d178f499ff385bc6ba3`  
		Last Modified: Thu, 23 Jul 2020 18:49:55 GMT  
		Size: 135.9 MB (135934696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1364c9d6721b53b1bd8778cb0d0ac87c86ed89e9dd342561ba2929dd95da275`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f945cae44a06e4c6a1675372333e392585e86f506b67a2e7318916725bee112`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc14-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:320e86de94f1766bc0b99968e01cc228a1c174d7ef03ca6fdea6b2beb79d19ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172898995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4556d6c47cee365c69938eff1c624edd885fccdf75221a14faeaa18799c1708a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:44:24 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Jul 2020 15:44:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:44:25 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:44:25 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:44:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:44:26 GMT
ENV MONGO_MAJOR=testing
# Fri, 24 Jul 2020 15:44:26 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Fri, 24 Jul 2020 15:44:26 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:46 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:52 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:52 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:52 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:53 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7846067e8c01b36594de6ff45d2d0009185a0a644f67e72d3f92d1b93632ee9e`  
		Last Modified: Fri, 24 Jul 2020 15:45:31 GMT  
		Size: 6.2 KB (6246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a2ff24811f96ec5c958284ebae49f0e4a05b93286c074721e96b9bec777827`  
		Last Modified: Fri, 24 Jul 2020 15:45:31 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e008bc650289579ec33129da28aec09626f0c279d9e50ad7f098f017ed49b3f1`  
		Last Modified: Fri, 24 Jul 2020 15:45:50 GMT  
		Size: 139.0 MB (139029683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fb3ee0131a773b21e3ecb0447a81b982bd346438608b31b807470e468b496c`  
		Last Modified: Fri, 24 Jul 2020 15:46:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885fab2cbb3ccf8839b04ab7a43fc58eb09741c03f40881c79b345aaba312863`  
		Last Modified: Fri, 24 Jul 2020 15:46:22 GMT  
		Size: 3.9 KB (3948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc14-windowsservercore`

```console
$ docker pull mongo@sha256:e6407858f33d264bd2be4d3b44d8ba99e7a6d5c889094a75e5638b8f3164847d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.4.0-rc14-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:172923a3c78e83de59a1e39e6db82e58a7133749ad9b41d320c03d257d3c44d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788364909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3ca42939f0b381c5792c06b47b048b23917e1da151bac43c13e9b86b478d7e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:17:03 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:17:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:17:05 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:30:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:30:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:30:53 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:30:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e03356e08c8f22ba6d71af8158646023fcc548e12f61c140007602c48873b3c`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d9c4688c8933a4e69cc3bd825ebab126557b6cefc7a7c0cde026d978442f8`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7686ce7eff68540ecbe87721a6c125c23c0ed14013f583241951500bad1b63c`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d2efade707503ce77b32f40675ffb6614e019fc90d911a2bb67b28f0e6715`  
		Last Modified: Thu, 23 Jul 2020 19:52:37 GMT  
		Size: 50.9 MB (50895014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22999ec35a51336544400b70143ef4695a2c45bef62861647214a3efa547d130`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a034beacfee6bc7401c5a99eb4ba13f78c0eb246f15ae1a8febf7ed2c6b4aa`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec07982643704a5e6385e3096821f7884d27d1a98a04c022c5a94defd2c10d1`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc14-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:aee6a672b5020ea8847a205151b2d825888c9437786b02a01a04b77539042833
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2722607823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6314d3e4e52f15d59bb1d397b078528323ca40e0104a13f54bce7738d8e411`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:31:04 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:31:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:31:07 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:49:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:49:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:49:07 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd666845ca3bdcc15c24652e0ff79e818b4d354ed8d9f00a9b78c0a69fb0dea1`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23643aa0c2818301a47e42fedeaa69d320141a602993824327ee39034d79d83`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ec84d6a917f6fc3d70328053e275180956b182e9c17814ab2ea3824d789b7`  
		Last Modified: Thu, 23 Jul 2020 19:52:48 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e99108a8f1ac902218296eabd2ca1661fa2c97d872ef52cf3b807e3146eda25`  
		Last Modified: Thu, 23 Jul 2020 19:53:33 GMT  
		Size: 412.4 MB (412407713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5c2cf8ea61e8374ec34fc6fa6fa5a44754721cec2905155ca79d847927087c`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455ff26c7051f08d062c946fa3968c4cc7aad659875c18e725b9b46a8508376e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111fda336322ed7db23e968ca25ce17c9a022ed20ba8caf1e8c523d00087a3e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc14-windowsservercore-1809`

```console
$ docker pull mongo@sha256:7e4ef9d5c5a99eaf5d7012f8d57cb4f55c5ef6ebbd3b1e357eef225555353b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.4.0-rc14-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:aee6a672b5020ea8847a205151b2d825888c9437786b02a01a04b77539042833
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2722607823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6314d3e4e52f15d59bb1d397b078528323ca40e0104a13f54bce7738d8e411`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:31:04 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:31:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:31:07 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:49:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:49:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:49:07 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd666845ca3bdcc15c24652e0ff79e818b4d354ed8d9f00a9b78c0a69fb0dea1`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23643aa0c2818301a47e42fedeaa69d320141a602993824327ee39034d79d83`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ec84d6a917f6fc3d70328053e275180956b182e9c17814ab2ea3824d789b7`  
		Last Modified: Thu, 23 Jul 2020 19:52:48 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e99108a8f1ac902218296eabd2ca1661fa2c97d872ef52cf3b807e3146eda25`  
		Last Modified: Thu, 23 Jul 2020 19:53:33 GMT  
		Size: 412.4 MB (412407713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5c2cf8ea61e8374ec34fc6fa6fa5a44754721cec2905155ca79d847927087c`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455ff26c7051f08d062c946fa3968c4cc7aad659875c18e725b9b46a8508376e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111fda336322ed7db23e968ca25ce17c9a022ed20ba8caf1e8c523d00087a3e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc14-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:152e497ecfcfc582cf4777a6570414f2bba75932558ef328a398b1f83f432fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:4.4.0-rc14-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:172923a3c78e83de59a1e39e6db82e58a7133749ad9b41d320c03d257d3c44d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788364909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3ca42939f0b381c5792c06b47b048b23917e1da151bac43c13e9b86b478d7e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:17:03 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:17:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:17:05 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:30:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:30:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:30:53 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:30:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e03356e08c8f22ba6d71af8158646023fcc548e12f61c140007602c48873b3c`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d9c4688c8933a4e69cc3bd825ebab126557b6cefc7a7c0cde026d978442f8`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7686ce7eff68540ecbe87721a6c125c23c0ed14013f583241951500bad1b63c`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d2efade707503ce77b32f40675ffb6614e019fc90d911a2bb67b28f0e6715`  
		Last Modified: Thu, 23 Jul 2020 19:52:37 GMT  
		Size: 50.9 MB (50895014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22999ec35a51336544400b70143ef4695a2c45bef62861647214a3efa547d130`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a034beacfee6bc7401c5a99eb4ba13f78c0eb246f15ae1a8febf7ed2c6b4aa`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec07982643704a5e6385e3096821f7884d27d1a98a04c022c5a94defd2c10d1`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc`

```console
$ docker pull mongo@sha256:c393c09247bd3e9071e7ce46b211bb79e34660e480daa8702b06f05cb5b614c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.4-rc` - linux; amd64

```console
$ docker pull mongo@sha256:bde690522196eb751b3c17689fa2e7b887f802b254518df50abaac9d82d9760c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177975003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c77712af1a38ff8f4cac7c28abb9787ff682cf389a107c58370780b69d36f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:29:13 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Jul 2020 16:29:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:29:15 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:29:15 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_MAJOR=testing
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Fri, 24 Jul 2020 16:29:16 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:40 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:40 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb942b17a59a8571f29488b50c40c51066e0efeac607b0bf0ac4100867d6fd3`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 6.3 KB (6251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2dae5231420c9acea900e9db4ad239422c3d80c23d91056980cfa09328b7ac`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb360f7104ab05ff0ed656a6a38f93c2d160d5bd667293780a0ebd6cb217029`  
		Last Modified: Fri, 24 Jul 2020 16:31:24 GMT  
		Size: 142.4 MB (142430756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05faea633d8b9266956c4d2a16aad66ef4f8dbc3b633290606f3ffb48e076968`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8546cbdb1cbcb75ad7cca67b243133c90007d5c6f1c36019a3538194ba1de34`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 4.0 KB (3951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b71539d673cad78259193407619c1ad22a50ff243f3916f93c5d5148ad9bc1cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167713824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb863a666bab8637029395a9356a3dd84606ecbc0f65aa80259f573d064a9490`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:16:53 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:16:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:16:56 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:16:57 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:58 GMT
ENV MONGO_MAJOR=testing
# Thu, 23 Jul 2020 18:46:45 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Thu, 23 Jul 2020 18:46:52 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:47:36 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:47:44 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:47:45 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:47:47 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:47:50 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:47:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c7dd9701ffc1428880bb0d6d480a9c5ed781b5a93786ddaf99a0e9fee5e5cf`  
		Last Modified: Mon, 06 Jul 2020 22:20:02 GMT  
		Size: 6.3 KB (6254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b64a1a43c684c5c8fb0b279ed8c7c4141ff239d79a1120ab3dfd300c44ba4`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a6906db4f2984ecfceded05cfbd9591acfd2d77617d178f499ff385bc6ba3`  
		Last Modified: Thu, 23 Jul 2020 18:49:55 GMT  
		Size: 135.9 MB (135934696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1364c9d6721b53b1bd8778cb0d0ac87c86ed89e9dd342561ba2929dd95da275`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f945cae44a06e4c6a1675372333e392585e86f506b67a2e7318916725bee112`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc` - linux; s390x

```console
$ docker pull mongo@sha256:320e86de94f1766bc0b99968e01cc228a1c174d7ef03ca6fdea6b2beb79d19ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172898995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4556d6c47cee365c69938eff1c624edd885fccdf75221a14faeaa18799c1708a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:44:24 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Jul 2020 15:44:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:44:25 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:44:25 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:44:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:44:26 GMT
ENV MONGO_MAJOR=testing
# Fri, 24 Jul 2020 15:44:26 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Fri, 24 Jul 2020 15:44:26 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:46 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:52 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:52 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:52 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:53 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7846067e8c01b36594de6ff45d2d0009185a0a644f67e72d3f92d1b93632ee9e`  
		Last Modified: Fri, 24 Jul 2020 15:45:31 GMT  
		Size: 6.2 KB (6246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a2ff24811f96ec5c958284ebae49f0e4a05b93286c074721e96b9bec777827`  
		Last Modified: Fri, 24 Jul 2020 15:45:31 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e008bc650289579ec33129da28aec09626f0c279d9e50ad7f098f017ed49b3f1`  
		Last Modified: Fri, 24 Jul 2020 15:45:50 GMT  
		Size: 139.0 MB (139029683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fb3ee0131a773b21e3ecb0447a81b982bd346438608b31b807470e468b496c`  
		Last Modified: Fri, 24 Jul 2020 15:46:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885fab2cbb3ccf8839b04ab7a43fc58eb09741c03f40881c79b345aaba312863`  
		Last Modified: Fri, 24 Jul 2020 15:46:22 GMT  
		Size: 3.9 KB (3948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:172923a3c78e83de59a1e39e6db82e58a7133749ad9b41d320c03d257d3c44d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788364909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3ca42939f0b381c5792c06b47b048b23917e1da151bac43c13e9b86b478d7e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:17:03 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:17:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:17:05 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:30:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:30:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:30:53 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:30:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e03356e08c8f22ba6d71af8158646023fcc548e12f61c140007602c48873b3c`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d9c4688c8933a4e69cc3bd825ebab126557b6cefc7a7c0cde026d978442f8`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7686ce7eff68540ecbe87721a6c125c23c0ed14013f583241951500bad1b63c`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d2efade707503ce77b32f40675ffb6614e019fc90d911a2bb67b28f0e6715`  
		Last Modified: Thu, 23 Jul 2020 19:52:37 GMT  
		Size: 50.9 MB (50895014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22999ec35a51336544400b70143ef4695a2c45bef62861647214a3efa547d130`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a034beacfee6bc7401c5a99eb4ba13f78c0eb246f15ae1a8febf7ed2c6b4aa`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec07982643704a5e6385e3096821f7884d27d1a98a04c022c5a94defd2c10d1`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:aee6a672b5020ea8847a205151b2d825888c9437786b02a01a04b77539042833
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2722607823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6314d3e4e52f15d59bb1d397b078528323ca40e0104a13f54bce7738d8e411`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:31:04 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:31:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:31:07 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:49:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:49:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:49:07 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd666845ca3bdcc15c24652e0ff79e818b4d354ed8d9f00a9b78c0a69fb0dea1`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23643aa0c2818301a47e42fedeaa69d320141a602993824327ee39034d79d83`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ec84d6a917f6fc3d70328053e275180956b182e9c17814ab2ea3824d789b7`  
		Last Modified: Thu, 23 Jul 2020 19:52:48 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e99108a8f1ac902218296eabd2ca1661fa2c97d872ef52cf3b807e3146eda25`  
		Last Modified: Thu, 23 Jul 2020 19:53:33 GMT  
		Size: 412.4 MB (412407713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5c2cf8ea61e8374ec34fc6fa6fa5a44754721cec2905155ca79d847927087c`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455ff26c7051f08d062c946fa3968c4cc7aad659875c18e725b9b46a8508376e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111fda336322ed7db23e968ca25ce17c9a022ed20ba8caf1e8c523d00087a3e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc-bionic`

```console
$ docker pull mongo@sha256:539e92ee53f9bd4bb10e8d89367dc8c82c3bea026feaa3b2d535468864cc7ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.4-rc-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:bde690522196eb751b3c17689fa2e7b887f802b254518df50abaac9d82d9760c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177975003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c77712af1a38ff8f4cac7c28abb9787ff682cf389a107c58370780b69d36f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:29:13 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Jul 2020 16:29:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:29:15 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:29:15 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_MAJOR=testing
# Fri, 24 Jul 2020 16:29:15 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Fri, 24 Jul 2020 16:29:16 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:40 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:40 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb942b17a59a8571f29488b50c40c51066e0efeac607b0bf0ac4100867d6fd3`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 6.3 KB (6251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2dae5231420c9acea900e9db4ad239422c3d80c23d91056980cfa09328b7ac`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb360f7104ab05ff0ed656a6a38f93c2d160d5bd667293780a0ebd6cb217029`  
		Last Modified: Fri, 24 Jul 2020 16:31:24 GMT  
		Size: 142.4 MB (142430756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05faea633d8b9266956c4d2a16aad66ef4f8dbc3b633290606f3ffb48e076968`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8546cbdb1cbcb75ad7cca67b243133c90007d5c6f1c36019a3538194ba1de34`  
		Last Modified: Fri, 24 Jul 2020 16:31:01 GMT  
		Size: 4.0 KB (3951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b71539d673cad78259193407619c1ad22a50ff243f3916f93c5d5148ad9bc1cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167713824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb863a666bab8637029395a9356a3dd84606ecbc0f65aa80259f573d064a9490`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:16:53 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 06 Jul 2020 22:16:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:16:56 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:16:57 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:58 GMT
ENV MONGO_MAJOR=testing
# Thu, 23 Jul 2020 18:46:45 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Thu, 23 Jul 2020 18:46:52 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 23 Jul 2020 18:47:36 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 23 Jul 2020 18:47:44 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 23 Jul 2020 18:47:45 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 Jul 2020 18:47:47 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Thu, 23 Jul 2020 18:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jul 2020 18:47:50 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 18:47:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c7dd9701ffc1428880bb0d6d480a9c5ed781b5a93786ddaf99a0e9fee5e5cf`  
		Last Modified: Mon, 06 Jul 2020 22:20:02 GMT  
		Size: 6.3 KB (6254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b64a1a43c684c5c8fb0b279ed8c7c4141ff239d79a1120ab3dfd300c44ba4`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a6906db4f2984ecfceded05cfbd9591acfd2d77617d178f499ff385bc6ba3`  
		Last Modified: Thu, 23 Jul 2020 18:49:55 GMT  
		Size: 135.9 MB (135934696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1364c9d6721b53b1bd8778cb0d0ac87c86ed89e9dd342561ba2929dd95da275`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f945cae44a06e4c6a1675372333e392585e86f506b67a2e7318916725bee112`  
		Last Modified: Thu, 23 Jul 2020 18:49:17 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:320e86de94f1766bc0b99968e01cc228a1c174d7ef03ca6fdea6b2beb79d19ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172898995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4556d6c47cee365c69938eff1c624edd885fccdf75221a14faeaa18799c1708a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:44:24 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Jul 2020 15:44:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:44:25 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:44:25 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:44:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:44:26 GMT
ENV MONGO_MAJOR=testing
# Fri, 24 Jul 2020 15:44:26 GMT
ENV MONGO_VERSION=4.4.0~rc14
# Fri, 24 Jul 2020 15:44:26 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:46 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:52 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:52 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:52 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:53 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7846067e8c01b36594de6ff45d2d0009185a0a644f67e72d3f92d1b93632ee9e`  
		Last Modified: Fri, 24 Jul 2020 15:45:31 GMT  
		Size: 6.2 KB (6246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a2ff24811f96ec5c958284ebae49f0e4a05b93286c074721e96b9bec777827`  
		Last Modified: Fri, 24 Jul 2020 15:45:31 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e008bc650289579ec33129da28aec09626f0c279d9e50ad7f098f017ed49b3f1`  
		Last Modified: Fri, 24 Jul 2020 15:45:50 GMT  
		Size: 139.0 MB (139029683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fb3ee0131a773b21e3ecb0447a81b982bd346438608b31b807470e468b496c`  
		Last Modified: Fri, 24 Jul 2020 15:46:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885fab2cbb3ccf8839b04ab7a43fc58eb09741c03f40881c79b345aaba312863`  
		Last Modified: Fri, 24 Jul 2020 15:46:22 GMT  
		Size: 3.9 KB (3948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc-windowsservercore`

```console
$ docker pull mongo@sha256:e6407858f33d264bd2be4d3b44d8ba99e7a6d5c889094a75e5638b8f3164847d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.4-rc-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:172923a3c78e83de59a1e39e6db82e58a7133749ad9b41d320c03d257d3c44d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788364909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3ca42939f0b381c5792c06b47b048b23917e1da151bac43c13e9b86b478d7e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:17:03 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:17:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:17:05 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:30:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:30:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:30:53 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:30:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e03356e08c8f22ba6d71af8158646023fcc548e12f61c140007602c48873b3c`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d9c4688c8933a4e69cc3bd825ebab126557b6cefc7a7c0cde026d978442f8`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7686ce7eff68540ecbe87721a6c125c23c0ed14013f583241951500bad1b63c`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d2efade707503ce77b32f40675ffb6614e019fc90d911a2bb67b28f0e6715`  
		Last Modified: Thu, 23 Jul 2020 19:52:37 GMT  
		Size: 50.9 MB (50895014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22999ec35a51336544400b70143ef4695a2c45bef62861647214a3efa547d130`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a034beacfee6bc7401c5a99eb4ba13f78c0eb246f15ae1a8febf7ed2c6b4aa`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec07982643704a5e6385e3096821f7884d27d1a98a04c022c5a94defd2c10d1`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:aee6a672b5020ea8847a205151b2d825888c9437786b02a01a04b77539042833
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2722607823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6314d3e4e52f15d59bb1d397b078528323ca40e0104a13f54bce7738d8e411`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:31:04 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:31:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:31:07 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:49:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:49:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:49:07 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd666845ca3bdcc15c24652e0ff79e818b4d354ed8d9f00a9b78c0a69fb0dea1`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23643aa0c2818301a47e42fedeaa69d320141a602993824327ee39034d79d83`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ec84d6a917f6fc3d70328053e275180956b182e9c17814ab2ea3824d789b7`  
		Last Modified: Thu, 23 Jul 2020 19:52:48 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e99108a8f1ac902218296eabd2ca1661fa2c97d872ef52cf3b807e3146eda25`  
		Last Modified: Thu, 23 Jul 2020 19:53:33 GMT  
		Size: 412.4 MB (412407713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5c2cf8ea61e8374ec34fc6fa6fa5a44754721cec2905155ca79d847927087c`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455ff26c7051f08d062c946fa3968c4cc7aad659875c18e725b9b46a8508376e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111fda336322ed7db23e968ca25ce17c9a022ed20ba8caf1e8c523d00087a3e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc-windowsservercore-1809`

```console
$ docker pull mongo@sha256:7e4ef9d5c5a99eaf5d7012f8d57cb4f55c5ef6ebbd3b1e357eef225555353b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:4.4-rc-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:aee6a672b5020ea8847a205151b2d825888c9437786b02a01a04b77539042833
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2722607823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6314d3e4e52f15d59bb1d397b078528323ca40e0104a13f54bce7738d8e411`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:31:04 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:31:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:31:07 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:49:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:49:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:49:07 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd666845ca3bdcc15c24652e0ff79e818b4d354ed8d9f00a9b78c0a69fb0dea1`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23643aa0c2818301a47e42fedeaa69d320141a602993824327ee39034d79d83`  
		Last Modified: Thu, 23 Jul 2020 19:52:50 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519ec84d6a917f6fc3d70328053e275180956b182e9c17814ab2ea3824d789b7`  
		Last Modified: Thu, 23 Jul 2020 19:52:48 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e99108a8f1ac902218296eabd2ca1661fa2c97d872ef52cf3b807e3146eda25`  
		Last Modified: Thu, 23 Jul 2020 19:53:33 GMT  
		Size: 412.4 MB (412407713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5c2cf8ea61e8374ec34fc6fa6fa5a44754721cec2905155ca79d847927087c`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455ff26c7051f08d062c946fa3968c4cc7aad659875c18e725b9b46a8508376e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111fda336322ed7db23e968ca25ce17c9a022ed20ba8caf1e8c523d00087a3e`  
		Last Modified: Thu, 23 Jul 2020 19:52:47 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:152e497ecfcfc582cf4777a6570414f2bba75932558ef328a398b1f83f432fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:4.4-rc-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:172923a3c78e83de59a1e39e6db82e58a7133749ad9b41d320c03d257d3c44d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788364909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3ca42939f0b381c5792c06b47b048b23917e1da151bac43c13e9b86b478d7e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jul 2020 19:17:03 GMT
ENV MONGO_VERSION=4.4.0-rc14
# Thu, 23 Jul 2020 19:17:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc14-signed.msi
# Thu, 23 Jul 2020 19:17:05 GMT
ENV MONGO_DOWNLOAD_SHA256=74febaa98cd4dc7095aa34c9451235e50f3fa5d662230b465800eba79b865a9d
# Thu, 23 Jul 2020 19:30:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 23 Jul 2020 19:30:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 23 Jul 2020 19:30:53 GMT
EXPOSE 27017
# Thu, 23 Jul 2020 19:30:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e03356e08c8f22ba6d71af8158646023fcc548e12f61c140007602c48873b3c`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d9c4688c8933a4e69cc3bd825ebab126557b6cefc7a7c0cde026d978442f8`  
		Last Modified: Thu, 23 Jul 2020 19:52:30 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7686ce7eff68540ecbe87721a6c125c23c0ed14013f583241951500bad1b63c`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d2efade707503ce77b32f40675ffb6614e019fc90d911a2bb67b28f0e6715`  
		Last Modified: Thu, 23 Jul 2020 19:52:37 GMT  
		Size: 50.9 MB (50895014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22999ec35a51336544400b70143ef4695a2c45bef62861647214a3efa547d130`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a034beacfee6bc7401c5a99eb4ba13f78c0eb246f15ae1a8febf7ed2c6b4aa`  
		Last Modified: Thu, 23 Jul 2020 19:52:27 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec07982643704a5e6385e3096821f7884d27d1a98a04c022c5a94defd2c10d1`  
		Last Modified: Thu, 23 Jul 2020 19:52:28 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-bionic`

```console
$ docker pull mongo@sha256:d5d4b6b5a8e19049338b966b55931fa5f24f21967cefdb4e61327bef69fb634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:1c2243a5e21884ffa532ca9d20c221b170d7b40774c235619f98e2f6eaec520a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164661608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee5b549543c004a3498f23961d4738978409070141182195f2305d4aeac452c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:28:41 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 16:28:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 16:28:44 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:03 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:03 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:03 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af4dac7d70ea6794e7f6f0099cf3efc142c887488b3f6509eb872a45d2019f`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3823edc3c66e56ba812abc32fc96b4c10dc01cb2a3db7396916f639308c6662c`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbddf980229c3970fd52f08bfdc828b86e8dea8a9d526867c914f41099ab9df0`  
		Last Modified: Fri, 24 Jul 2020 16:30:56 GMT  
		Size: 129.1 MB (129122186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b1b60b739655778edd0020061c2381f1b2727657aa7d029b5e9e2a8a5a94d`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4592ef90c0ade4aaeac77b7c6dc9fd19234e2c0fdbbdd0cc8fd9e08870765120`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ff751a2fb9620cf8c8365e63d4e04b469246ca11d3fd3c778cde03a48f2006aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154674414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb889e5df20c6183f51f33be954ff870118609f845487614c8386f611946c6eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:15:56 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Mon, 06 Jul 2020 22:15:58 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:01 GMT
ENV MONGO_MAJOR=4.2
# Mon, 06 Jul 2020 22:16:02 GMT
ENV MONGO_VERSION=4.2.8
# Mon, 06 Jul 2020 22:16:04 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:16:29 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:16:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:16:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:16:34 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:16:36 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:16:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da8dd3b9fe4a2caac5977b8fd0ee6db66375a71cbb02c62717932c320f2343`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da5789bf40ba9ce0f4fa625e5d6e3a0736dc3e2d98c210c4f38e4285bc287c0`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0f9c45625791804dba83db5be92e028c9fec1682eb0030f8dfadabc454f49`  
		Last Modified: Mon, 06 Jul 2020 22:19:35 GMT  
		Size: 122.9 MB (122900108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d04d449a2731ebdc8507f7fb40a361de38d09987064ac93f8d039c295a2717`  
		Last Modified: Mon, 06 Jul 2020 22:19:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e28a037deb6b57194eb44b2769d3fb253fad9a2385b3b5a457b89c137a1376`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:5db5812120b93c55c30b1b8626d7282704a6257d9679620b089cece050dfc3ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160602549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b37e732dec18de7fb04cbd6aeb6fc1fdf94f48de0e6725a7b9a29ae25dc0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:43:46 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 15:43:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 15:43:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:07 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:12 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:12 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:12 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ee891f925f24ddc2e8ccf8702934c12f13c780740bf68f160f4e5c5fe2ae`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a811584177c153f52f80ad54cea747d45227e567aa751413e4b6f45b93c31`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09fc4e97d3b4ad9658f9148e7b5a9141b09c97405b347246e532e78d41654c`  
		Last Modified: Fri, 24 Jul 2020 15:45:22 GMT  
		Size: 126.7 MB (126738049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0f29fcd01f15d95c9e432a029579555b523f7d62bc53c23df060c2e005c54`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a235bd7958c88d38f7f3c3886c775a56e1f018884bf8bd31334822677e18654`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 3.9 KB (3949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:ff58ef6f07de1f251dbccead1949f582e75519bfd18b82cd6dd03f46f53784e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:8d7f9b3710dcd74d916c3f250672932aa3d646eacad6fe9c25a0734e416c9d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:f06909500296ef95416990ad20e3fc408027df1f49a882c7f75137f7dfb21862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:4-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:bionic`

```console
$ docker pull mongo@sha256:d5d4b6b5a8e19049338b966b55931fa5f24f21967cefdb4e61327bef69fb634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:bionic` - linux; amd64

```console
$ docker pull mongo@sha256:1c2243a5e21884ffa532ca9d20c221b170d7b40774c235619f98e2f6eaec520a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164661608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee5b549543c004a3498f23961d4738978409070141182195f2305d4aeac452c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:28:41 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 16:28:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 16:28:44 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:03 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:03 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:03 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af4dac7d70ea6794e7f6f0099cf3efc142c887488b3f6509eb872a45d2019f`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3823edc3c66e56ba812abc32fc96b4c10dc01cb2a3db7396916f639308c6662c`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbddf980229c3970fd52f08bfdc828b86e8dea8a9d526867c914f41099ab9df0`  
		Last Modified: Fri, 24 Jul 2020 16:30:56 GMT  
		Size: 129.1 MB (129122186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b1b60b739655778edd0020061c2381f1b2727657aa7d029b5e9e2a8a5a94d`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4592ef90c0ade4aaeac77b7c6dc9fd19234e2c0fdbbdd0cc8fd9e08870765120`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ff751a2fb9620cf8c8365e63d4e04b469246ca11d3fd3c778cde03a48f2006aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154674414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb889e5df20c6183f51f33be954ff870118609f845487614c8386f611946c6eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:15:56 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Mon, 06 Jul 2020 22:15:58 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:01 GMT
ENV MONGO_MAJOR=4.2
# Mon, 06 Jul 2020 22:16:02 GMT
ENV MONGO_VERSION=4.2.8
# Mon, 06 Jul 2020 22:16:04 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:16:29 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:16:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:16:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:16:34 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:16:36 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:16:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da8dd3b9fe4a2caac5977b8fd0ee6db66375a71cbb02c62717932c320f2343`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da5789bf40ba9ce0f4fa625e5d6e3a0736dc3e2d98c210c4f38e4285bc287c0`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0f9c45625791804dba83db5be92e028c9fec1682eb0030f8dfadabc454f49`  
		Last Modified: Mon, 06 Jul 2020 22:19:35 GMT  
		Size: 122.9 MB (122900108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d04d449a2731ebdc8507f7fb40a361de38d09987064ac93f8d039c295a2717`  
		Last Modified: Mon, 06 Jul 2020 22:19:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e28a037deb6b57194eb44b2769d3fb253fad9a2385b3b5a457b89c137a1376`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; s390x

```console
$ docker pull mongo@sha256:5db5812120b93c55c30b1b8626d7282704a6257d9679620b089cece050dfc3ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160602549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b37e732dec18de7fb04cbd6aeb6fc1fdf94f48de0e6725a7b9a29ae25dc0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:43:46 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 15:43:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 15:43:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:07 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:12 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:12 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:12 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ee891f925f24ddc2e8ccf8702934c12f13c780740bf68f160f4e5c5fe2ae`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a811584177c153f52f80ad54cea747d45227e567aa751413e4b6f45b93c31`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09fc4e97d3b4ad9658f9148e7b5a9141b09c97405b347246e532e78d41654c`  
		Last Modified: Fri, 24 Jul 2020 15:45:22 GMT  
		Size: 126.7 MB (126738049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0f29fcd01f15d95c9e432a029579555b523f7d62bc53c23df060c2e005c54`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a235bd7958c88d38f7f3c3886c775a56e1f018884bf8bd31334822677e18654`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 3.9 KB (3949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:latest`

```console
$ docker pull mongo@sha256:41f8e979f23624d1da534fee1b1e5c8d734173e18c510c1ababd375bba585534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:1c2243a5e21884ffa532ca9d20c221b170d7b40774c235619f98e2f6eaec520a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164661608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee5b549543c004a3498f23961d4738978409070141182195f2305d4aeac452c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:28:19 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 16:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:28:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 16:28:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 16:28:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 16:28:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 16:28:41 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 16:28:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 16:28:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 16:28:43 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 16:28:44 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 16:29:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 16:29:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 16:29:03 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 16:29:03 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 16:29:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 16:29:03 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 16:29:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8718c532d71807a7a4e0b08f660bb11ec406ee134e947459d2fe0d27b99d440`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9035443a91bc2dca29aa6d8e8609c5c7af34b497342f12b1a5a668e4c24b04b5`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 3.0 MB (2973801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca553166d9ffa1d03ce6638fb2a72cd8fbd699a0de622e21222c3c6be306cf`  
		Last Modified: Fri, 24 Jul 2020 16:30:40 GMT  
		Size: 5.8 MB (5824368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc866a5c284c73c09a3a10ac11e49f2ab972a9de9563585cd977f4a6e47909ea`  
		Last Modified: Fri, 24 Jul 2020 16:30:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8af4dac7d70ea6794e7f6f0099cf3efc142c887488b3f6509eb872a45d2019f`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3823edc3c66e56ba812abc32fc96b4c10dc01cb2a3db7396916f639308c6662c`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbddf980229c3970fd52f08bfdc828b86e8dea8a9d526867c914f41099ab9df0`  
		Last Modified: Fri, 24 Jul 2020 16:30:56 GMT  
		Size: 129.1 MB (129122186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b1b60b739655778edd0020061c2381f1b2727657aa7d029b5e9e2a8a5a94d`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4592ef90c0ade4aaeac77b7c6dc9fd19234e2c0fdbbdd0cc8fd9e08870765120`  
		Last Modified: Fri, 24 Jul 2020 16:30:38 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ff751a2fb9620cf8c8365e63d4e04b469246ca11d3fd3c778cde03a48f2006aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154674414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb889e5df20c6183f51f33be954ff870118609f845487614c8386f611946c6eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:15:05 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 06 Jul 2020 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:15:22 GMT
ENV GOSU_VERSION=1.12
# Mon, 06 Jul 2020 22:15:22 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Jul 2020 22:15:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 06 Jul 2020 22:15:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 06 Jul 2020 22:15:56 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Mon, 06 Jul 2020 22:15:58 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Jul 2020 22:15:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Jul 2020 22:16:01 GMT
ENV MONGO_MAJOR=4.2
# Mon, 06 Jul 2020 22:16:02 GMT
ENV MONGO_VERSION=4.2.8
# Mon, 06 Jul 2020 22:16:04 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 06 Jul 2020 22:16:29 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 06 Jul 2020 22:16:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 06 Jul 2020 22:16:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Jul 2020 22:16:34 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 06 Jul 2020 22:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jul 2020 22:16:36 GMT
EXPOSE 27017
# Mon, 06 Jul 2020 22:16:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39459711a4d84feeec346967cc5d168ab630787692ac9d7046ce8d69fae32ce6`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5911789bebe2ea39a92d6311498dec854edb65ad1b7191710743068f3bdbce9f`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 2.7 MB (2665652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccca654cc654092efbbe9d5764645936ec9d17344579e93a74632edae5fd662`  
		Last Modified: Mon, 06 Jul 2020 22:19:11 GMT  
		Size: 5.3 MB (5345226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c607c92b45766c4f7436ba454d829197fd94766b22a23b04f6374e3e96cb5`  
		Last Modified: Mon, 06 Jul 2020 22:19:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da8dd3b9fe4a2caac5977b8fd0ee6db66375a71cbb02c62717932c320f2343`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da5789bf40ba9ce0f4fa625e5d6e3a0736dc3e2d98c210c4f38e4285bc287c0`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0f9c45625791804dba83db5be92e028c9fec1682eb0030f8dfadabc454f49`  
		Last Modified: Mon, 06 Jul 2020 22:19:35 GMT  
		Size: 122.9 MB (122900108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d04d449a2731ebdc8507f7fb40a361de38d09987064ac93f8d039c295a2717`  
		Last Modified: Mon, 06 Jul 2020 22:19:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e28a037deb6b57194eb44b2769d3fb253fad9a2385b3b5a457b89c137a1376`  
		Last Modified: Mon, 06 Jul 2020 22:19:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; s390x

```console
$ docker pull mongo@sha256:5db5812120b93c55c30b1b8626d7282704a6257d9679620b089cece050dfc3ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160602549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b37e732dec18de7fb04cbd6aeb6fc1fdf94f48de0e6725a7b9a29ae25dc0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:43:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Jul 2020 15:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:43:24 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Jul 2020 15:43:24 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Jul 2020 15:43:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jul 2020 15:43:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jul 2020 15:43:46 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Jul 2020 15:43:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Jul 2020 15:43:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Jul 2020 15:43:48 GMT
ENV MONGO_VERSION=4.2.8
# Fri, 24 Jul 2020 15:43:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Jul 2020 15:44:07 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Jul 2020 15:44:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Jul 2020 15:44:12 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Jul 2020 15:44:12 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Jul 2020 15:44:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jul 2020 15:44:12 GMT
EXPOSE 27017
# Fri, 24 Jul 2020 15:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d142c8697105ff1f23ed9bd276c79403229ef5a4d41c41086e09ad2444a996f`  
		Last Modified: Fri, 24 Jul 2020 15:45:13 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc340eb9fd01be2020add2839f3ce38a28ded5dc339a7503d147aef44ad1a296`  
		Last Modified: Fri, 24 Jul 2020 15:45:12 GMT  
		Size: 2.7 MB (2704645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f52a59dd29fc61ae5f488818a53d49fbf8ab5b3ff7521cf5cf3579b2563d98`  
		Last Modified: Fri, 24 Jul 2020 15:45:11 GMT  
		Size: 5.7 MB (5745306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946e9c18d062252598ff3379b08f123b3b7b6dbae9da49243131e83a831ae21a`  
		Last Modified: Fri, 24 Jul 2020 15:45:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ee891f925f24ddc2e8ccf8702934c12f13c780740bf68f160f4e5c5fe2ae`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a811584177c153f52f80ad54cea747d45227e567aa751413e4b6f45b93c31`  
		Last Modified: Fri, 24 Jul 2020 15:45:08 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09fc4e97d3b4ad9658f9148e7b5a9141b09c97405b347246e532e78d41654c`  
		Last Modified: Fri, 24 Jul 2020 15:45:22 GMT  
		Size: 126.7 MB (126738049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0f29fcd01f15d95c9e432a029579555b523f7d62bc53c23df060c2e005c54`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a235bd7958c88d38f7f3c3886c775a56e1f018884bf8bd31334822677e18654`  
		Last Modified: Fri, 24 Jul 2020 15:45:24 GMT  
		Size: 3.9 KB (3949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:ff58ef6f07de1f251dbccead1949f582e75519bfd18b82cd6dd03f46f53784e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:8d7f9b3710dcd74d916c3f250672932aa3d646eacad6fe9c25a0734e416c9d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:f06909500296ef95416990ad20e3fc408027df1f49a882c7f75137f7dfb21862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
