## `redis:6-buster`

```console
$ docker pull redis@sha256:062de5c3b9c4bb9bbd4f216fa5413384b96134d3e057b440f7c34b511b2e23e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:6-buster` - linux; amd64

```console
$ docker pull redis@sha256:45aa14edd613e474653c9b927920861dab0951e8d679d94425b369d1ed226541
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38168197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c349430fd524ffbdda332e6a6b037e14c07244dc0c37a7e24152fbb1dc1c3c05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 20:45:33 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 09 Jun 2020 20:45:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Jun 2020 20:45:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Jun 2020 20:45:46 GMT
ENV REDIS_VERSION=6.0.4
# Tue, 09 Jun 2020 20:45:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.4.tar.gz
# Tue, 09 Jun 2020 20:45:47 GMT
ENV REDIS_DOWNLOAD_SHA=3337005a1e0c3aa293c87c313467ea8ac11984921fab08807998ba765c9943de
# Tue, 09 Jun 2020 20:46:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 09 Jun 2020 20:46:55 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 09 Jun 2020 20:46:55 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 20:46:56 GMT
WORKDIR /data
# Tue, 09 Jun 2020 20:46:56 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 09 Jun 2020 20:46:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 20:46:56 GMT
EXPOSE 6379
# Tue, 09 Jun 2020 20:46:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a6a5c53ff0d7433fa114f3d8b94992deda869addc164bd15ce40e2f72f0fd6`  
		Last Modified: Tue, 09 Jun 2020 20:50:12 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69876b7abed8f17b52974bf0be00fcaf4d2d3d622bd2349c8e16407331e8b88`  
		Last Modified: Tue, 09 Jun 2020 20:50:12 GMT  
		Size: 1.4 MB (1417666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f590ddd7edb2c7add3f256badeaadf4b07690c01ed8dfa824eaa6404f0cc38d`  
		Last Modified: Tue, 09 Jun 2020 20:50:14 GMT  
		Size: 9.7 MB (9650034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28bb38e9c0d4399d6b96e18acf72c8d5e876909ed124ad499ca67449a4d3c0f`  
		Last Modified: Tue, 09 Jun 2020 20:50:12 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bcff1416bf7f588ea84c0a13b20a5e15315ca1f341a5fddc9c0c468bae06b`  
		Last Modified: Tue, 09 Jun 2020 20:50:13 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; arm variant v5

```console
$ docker pull redis@sha256:bd405bb99be0ed8721304a23d4a0b225074cb0a097b9703015833dcf299a15de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35393175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c93af33efa282d1fe538ea56c3399b4c360d8f0e7f22735c7a4d898ac5088c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jun 2020 00:51:58 GMT
ADD file:7fde417d1c70a9ef2b4e468f6e2ee4cbd3f340fb2d5b67ede087c81520c95f4a in / 
# Tue, 09 Jun 2020 00:51:59 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:13:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 09 Jun 2020 07:13:31 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Jun 2020 07:14:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Jun 2020 07:14:04 GMT
ENV REDIS_VERSION=6.0.4
# Tue, 09 Jun 2020 07:14:05 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.4.tar.gz
# Tue, 09 Jun 2020 07:14:06 GMT
ENV REDIS_DOWNLOAD_SHA=3337005a1e0c3aa293c87c313467ea8ac11984921fab08807998ba765c9943de
# Tue, 09 Jun 2020 07:15:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 09 Jun 2020 07:15:22 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 09 Jun 2020 07:15:23 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 07:15:24 GMT
WORKDIR /data
# Tue, 09 Jun 2020 07:15:25 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:15:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:15:27 GMT
EXPOSE 6379
# Tue, 09 Jun 2020 07:15:28 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5b11fc09c1a26b11a7df7d593adf43baff53c5cdba71cf8a87ae4a6dd17eb52c`  
		Last Modified: Tue, 09 Jun 2020 00:59:24 GMT  
		Size: 24.8 MB (24837249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bacb18640994730a015fc7704e0cef48a50c2a829dc127acff37988f85a58cc`  
		Last Modified: Tue, 09 Jun 2020 07:17:29 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862b2b6c212df122d0cc5b0bc23864c5874de338f17b0dfa7da836aeca0b9f98`  
		Last Modified: Tue, 09 Jun 2020 07:17:29 GMT  
		Size: 1.4 MB (1376094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7174457491ead2dbd3d47310ce153b46323df983cd041dfece1c54c3eb4e5c8`  
		Last Modified: Tue, 09 Jun 2020 07:17:32 GMT  
		Size: 9.2 MB (9177571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b5fd7ad6f09115abf5a2771c8ef2d923f5ccb238b305829246cdef741d1d9`  
		Last Modified: Tue, 09 Jun 2020 07:17:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb390861393e043ba516ddf23e9c9460188c10f87022696800c227cf9930b2c`  
		Last Modified: Tue, 09 Jun 2020 07:17:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; arm variant v7

```console
$ docker pull redis@sha256:62d8624ab416d490283fc7ea97ef657ebe13b742289c5c12ae9fab7d7da11cf2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2225a9a2492080c80f37ce04a666614b5cbcf81fd7e384cb663e48f238e897`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 18:26:54 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 09 Jun 2020 18:26:55 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Jun 2020 18:27:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Jun 2020 18:27:25 GMT
ENV REDIS_VERSION=6.0.4
# Tue, 09 Jun 2020 18:27:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.4.tar.gz
# Tue, 09 Jun 2020 18:27:27 GMT
ENV REDIS_DOWNLOAD_SHA=3337005a1e0c3aa293c87c313467ea8ac11984921fab08807998ba765c9943de
# Tue, 09 Jun 2020 18:28:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 09 Jun 2020 18:28:35 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 09 Jun 2020 18:28:36 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 18:28:36 GMT
WORKDIR /data
# Tue, 09 Jun 2020 18:28:37 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 09 Jun 2020 18:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 18:28:39 GMT
EXPOSE 6379
# Tue, 09 Jun 2020 18:28:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3327f7a496f3f9a645339962c5ff7707e5d3d8527605c0b61e2437df8d05d57e`  
		Last Modified: Tue, 09 Jun 2020 18:30:56 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ad81e0d5836d20a5deab240146c524b20f1c4eb3fcdab4fd05f9e7567e9a1e`  
		Last Modified: Tue, 09 Jun 2020 18:30:41 GMT  
		Size: 1.4 MB (1368141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb60d75bd686eaf311093876be5a29de940b98a1f831c3ac3ae5824e3918159`  
		Last Modified: Tue, 09 Jun 2020 18:30:41 GMT  
		Size: 8.9 MB (8942309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354a6158ac5f6a649fbc5485956066450ab0718cf126ff0e17d664ee67efb7f6`  
		Last Modified: Tue, 09 Jun 2020 18:30:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b9515157e28dc970eada949b71e883f813645e11facaff6a4a60505c5a6c36`  
		Last Modified: Tue, 09 Jun 2020 18:30:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:b2dba7f68ed3d6de7588bb3a537ca07630e5d49d6c0f50de19a4819a1b2d5137
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36726461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aff2bb8ea682d762e0ccd27647aa1f9815800da85f65c226a36cac8b5e5814f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 13:59:52 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 09 Jun 2020 13:59:53 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Jun 2020 14:00:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Jun 2020 14:00:24 GMT
ENV REDIS_VERSION=6.0.4
# Tue, 09 Jun 2020 14:00:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.4.tar.gz
# Tue, 09 Jun 2020 14:00:27 GMT
ENV REDIS_DOWNLOAD_SHA=3337005a1e0c3aa293c87c313467ea8ac11984921fab08807998ba765c9943de
# Tue, 09 Jun 2020 14:01:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 09 Jun 2020 14:01:50 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 09 Jun 2020 14:01:51 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 14:01:52 GMT
WORKDIR /data
# Tue, 09 Jun 2020 14:01:53 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 09 Jun 2020 14:01:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 14:01:54 GMT
EXPOSE 6379
# Tue, 09 Jun 2020 14:01:55 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd20313beb311f9333c1f47bbe7694bb922e79f5403daa59e5e16ff79e9db43`  
		Last Modified: Tue, 09 Jun 2020 14:04:40 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d34e6a8c07fe57114baaa650962827351af5046989cc2361d695a748ecac04`  
		Last Modified: Tue, 09 Jun 2020 14:04:41 GMT  
		Size: 1.4 MB (1352908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586c9a22928d7191ffb7a39bda4fa56fb08f562d7ea6ecd465acebcb240cf1a`  
		Last Modified: Tue, 09 Jun 2020 14:04:44 GMT  
		Size: 9.5 MB (9513579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6ea0251d7dc0c7528bf176140cc3caec255e47ec64473e82521640d7b9b3bb`  
		Last Modified: Tue, 09 Jun 2020 14:04:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45320d77d1b80c87d9b5a9c6153ec3f0a5ecfd852bbb5b389b00fb22f709c91`  
		Last Modified: Tue, 09 Jun 2020 14:04:41 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; 386

```console
$ docker pull redis@sha256:ef75d0de117262fcc5d7caf02fdd0a372b6204dfc28c677ba370a5665c6794db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38428134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca29dc0c9c444fcbafe320a53239291b47ed554b3bf6ba7edc459d02e8f12563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 19:43:46 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 09 Jun 2020 19:43:46 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Jun 2020 19:44:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Jun 2020 19:44:06 GMT
ENV REDIS_VERSION=6.0.4
# Tue, 09 Jun 2020 19:44:07 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.4.tar.gz
# Tue, 09 Jun 2020 19:44:07 GMT
ENV REDIS_DOWNLOAD_SHA=3337005a1e0c3aa293c87c313467ea8ac11984921fab08807998ba765c9943de
# Tue, 09 Jun 2020 19:46:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 09 Jun 2020 19:46:02 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 09 Jun 2020 19:46:02 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 19:46:02 GMT
WORKDIR /data
# Tue, 09 Jun 2020 19:46:03 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 09 Jun 2020 19:46:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 19:46:04 GMT
EXPOSE 6379
# Tue, 09 Jun 2020 19:46:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41be782ae7e5ade04fdcb9a1b7e47dfc657577d52ca2c56e69bc15d6ff0d9ab`  
		Last Modified: Tue, 09 Jun 2020 19:48:25 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482c539a928e9561b259316816a6933b2cd8ddd0d703ebc73aa310db2c8c7cd`  
		Last Modified: Tue, 09 Jun 2020 19:48:26 GMT  
		Size: 1.4 MB (1387452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531d22907bc053c15b049190e376cb92b99178ded105def070de77ef1b3d5b18`  
		Last Modified: Tue, 09 Jun 2020 19:48:29 GMT  
		Size: 9.3 MB (9283546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0c6b022553bf08ec3dbc55a8f0458ea6d488046d27711431a2bb70325fe01d`  
		Last Modified: Tue, 09 Jun 2020 19:48:26 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d26857e68c4876cd51825b3595b5dcc1a23e9aff5c2d7ab466e9d0bdc1f67f`  
		Last Modified: Tue, 09 Jun 2020 19:48:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; mips64le

```console
$ docker pull redis@sha256:91f01645d747d92d75b04817c86d68308765abec16b61fe9c8177c19381f33d2
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36603546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560c688917fe5e021f497a256fa903f84a61a4555ae85f372c170fe7d587eddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jun 2020 01:10:06 GMT
ADD file:faf18b832680e98050b98c329add242425904e64c6a5a491c22d33e9417ef323 in / 
# Tue, 09 Jun 2020 01:10:06 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 20:51:21 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 09 Jun 2020 20:51:21 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Jun 2020 20:51:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Jun 2020 20:51:49 GMT
ENV REDIS_VERSION=6.0.4
# Tue, 09 Jun 2020 20:51:49 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.4.tar.gz
# Tue, 09 Jun 2020 20:51:50 GMT
ENV REDIS_DOWNLOAD_SHA=3337005a1e0c3aa293c87c313467ea8ac11984921fab08807998ba765c9943de
# Tue, 09 Jun 2020 20:55:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 09 Jun 2020 20:55:18 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 09 Jun 2020 20:55:18 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 20:55:18 GMT
WORKDIR /data
# Tue, 09 Jun 2020 20:55:19 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 09 Jun 2020 20:55:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 20:55:20 GMT
EXPOSE 6379
# Tue, 09 Jun 2020 20:55:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:76f2a0c8ea98ebd699a77ced9c677e97cd54b038a8c5e89670af78f38b047b33`  
		Last Modified: Tue, 09 Jun 2020 01:18:14 GMT  
		Size: 25.8 MB (25764040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98037b32ce5f6bbc4cdfb87147f17d72d114cc4631d91a4f55385aa5abc97efa`  
		Last Modified: Tue, 09 Jun 2020 20:59:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe4ce897d62a8f1adc5d381f61c4a6ce437a73cfdf7775f5fc96ebde1fc7c7`  
		Last Modified: Tue, 09 Jun 2020 20:59:13 GMT  
		Size: 1.3 MB (1305400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6322196684d6ad53c94e55be85f94f1833f92dbebf746245a3bdb9630fcbbc`  
		Last Modified: Tue, 09 Jun 2020 20:59:20 GMT  
		Size: 9.5 MB (9531874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d030d26946f2fdd1a5ff98a5ba368d2e72252d11e36f30e08fa24ac402fd1`  
		Last Modified: Tue, 09 Jun 2020 20:59:12 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c8b6f53cd0a00deede646960e02e5eda2227eb096705f955e9805bb39fd7f`  
		Last Modified: Tue, 09 Jun 2020 20:59:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; ppc64le

```console
$ docker pull redis@sha256:2e6175e00d6de544a079d74299c09efc6c569b7b1ecd1933e6467565b0019369
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac06567e8f25f93ac59688e9dae7392e485a2f7feb93916dc5cf883ce1323881`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:34 GMT
ADD file:796aad1a35ba276b8cccc19987c152a713db101b2b65e30923db753f5b7f4b0f in / 
# Tue, 09 Jun 2020 01:22:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 17:49:43 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 09 Jun 2020 17:49:49 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Jun 2020 17:52:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Jun 2020 17:52:33 GMT
ENV REDIS_VERSION=6.0.4
# Tue, 09 Jun 2020 17:52:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.4.tar.gz
# Tue, 09 Jun 2020 17:52:41 GMT
ENV REDIS_DOWNLOAD_SHA=3337005a1e0c3aa293c87c313467ea8ac11984921fab08807998ba765c9943de
# Tue, 09 Jun 2020 17:54:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 09 Jun 2020 17:55:04 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 09 Jun 2020 17:55:10 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 17:55:13 GMT
WORKDIR /data
# Tue, 09 Jun 2020 17:55:14 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 09 Jun 2020 17:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 17:55:20 GMT
EXPOSE 6379
# Tue, 09 Jun 2020 17:55:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:63dbb66c5119bb5086d9e6fb6b154211afc20b44ed136ab7df808f6044cfc6f1`  
		Last Modified: Tue, 09 Jun 2020 01:31:04 GMT  
		Size: 30.5 MB (30524405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bd07740270c2e091dd2d53ff514e569ab6317f8e13127325c02b8f373799e7`  
		Last Modified: Tue, 09 Jun 2020 17:59:27 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7577888307f392a71a9e051a2635001440b124e3b3ae5cb3e10e8dca0906a`  
		Last Modified: Tue, 09 Jun 2020 17:59:27 GMT  
		Size: 1.3 MB (1335381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674aee78df65d7f5faf479747d8d94f7ddd92cd0bd1ad363b85a856e3ffd2cdf`  
		Last Modified: Tue, 09 Jun 2020 17:59:30 GMT  
		Size: 10.3 MB (10255616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fec4f9585b26d76a26854dac191427a311fe07013dc4afb29e9ee93af2b51b`  
		Last Modified: Tue, 09 Jun 2020 17:59:27 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d7aff8b307f2113b7a352bc79d0bc944321e12ab13457d7498ecab47aa0380`  
		Last Modified: Tue, 09 Jun 2020 17:59:27 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; s390x

```console
$ docker pull redis@sha256:73ea2c3ffa7bda3fe49309a06123799e24e184b38f91a123afcd784fd5f14d32
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36741951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37e3cd2db03ec0c2e6ea6aae7a51d66b64de9339ad27a8581014bd2b4d52317`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:37 GMT
ADD file:b21d426de40a194c6c76ed27593f33fb1ea470e15d4d43b00d7601472110de1a in / 
# Tue, 09 Jun 2020 01:42:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 11:26:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 09 Jun 2020 11:26:40 GMT
ENV GOSU_VERSION=1.12
# Tue, 09 Jun 2020 11:27:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 09 Jun 2020 11:27:06 GMT
ENV REDIS_VERSION=6.0.4
# Tue, 09 Jun 2020 11:27:07 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.4.tar.gz
# Tue, 09 Jun 2020 11:27:08 GMT
ENV REDIS_DOWNLOAD_SHA=3337005a1e0c3aa293c87c313467ea8ac11984921fab08807998ba765c9943de
# Tue, 09 Jun 2020 11:28:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 09 Jun 2020 11:28:15 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 09 Jun 2020 11:28:15 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 11:28:16 GMT
WORKDIR /data
# Tue, 09 Jun 2020 11:28:17 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:28:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 11:28:18 GMT
EXPOSE 6379
# Tue, 09 Jun 2020 11:28:19 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:405e75bf6bb0104d67fcebf58e07cd21bf344589df9c1a41c00354a60ea3a604`  
		Last Modified: Tue, 09 Jun 2020 01:46:30 GMT  
		Size: 25.7 MB (25712668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03733ea6a63584425902e780cf1a3270cc136085ca96c08c11f1c3723424865e`  
		Last Modified: Tue, 09 Jun 2020 11:30:19 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c641f1df61fc7d52d72d38d2f33f5eda5d07c734b49cb8a6c27ab19dd4a82b6`  
		Last Modified: Tue, 09 Jun 2020 11:30:19 GMT  
		Size: 1.4 MB (1403809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de547d72bcd5106adbb3fd324cf7a3f2db407f390491987aeb4eae22042255`  
		Last Modified: Tue, 09 Jun 2020 11:30:21 GMT  
		Size: 9.6 MB (9623204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e4b59d8d41dece66d2b0f764b5ecc7987712a9e64ca5e2e2bd77ed6d99ca63`  
		Last Modified: Tue, 09 Jun 2020 11:30:24 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5513986bc03d03338f094ca404f6c251317657c4bcdeeb2b7ab4e684cd99a650`  
		Last Modified: Tue, 09 Jun 2020 11:30:24 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
