## `redis:5-alpine`

```console
$ docker pull redis@sha256:a1c13d4ebf3862b542d3a177710c91246f3f14217954a93a2e3bf956d634ff38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:5-alpine` - linux; amd64

```console
$ docker pull redis@sha256:2aad71790f042b4423face7fccfe77ea8984f628b719280b43f11de0f6803146
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcec99c5637388ae43f4a28837d9a0c518c56bba641933e08569a751ba8f87da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:27:29 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 26 Mar 2021 07:27:30 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 26 Mar 2021 07:29:49 GMT
ENV REDIS_VERSION=5.0.12
# Fri, 26 Mar 2021 07:29:49 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Fri, 26 Mar 2021 07:29:49 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Fri, 26 Mar 2021 07:30:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 26 Mar 2021 07:30:42 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 26 Mar 2021 07:30:42 GMT
VOLUME [/data]
# Fri, 26 Mar 2021 07:30:43 GMT
WORKDIR /data
# Fri, 26 Mar 2021 07:30:43 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 26 Mar 2021 07:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:30:43 GMT
EXPOSE 6379
# Fri, 26 Mar 2021 07:30:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201a3f4cf4c20b71abece6260944bd35ed5157fcde3cf12ca8e4b653ec24f6b8`  
		Last Modified: Fri, 26 Mar 2021 07:31:35 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14d413c86584055aaeda201bec1bbe19ac92cc049eee3f4e4bf5b81a6ed7d8e`  
		Last Modified: Fri, 26 Mar 2021 07:31:35 GMT  
		Size: 384.2 KB (384180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8695534d2cf37850e21f46c08791e67ee71ef39e81084b76a24c61376c170e`  
		Last Modified: Fri, 26 Mar 2021 07:32:34 GMT  
		Size: 6.6 MB (6642212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6544c9f87bec34e0e68894969610d6ba05d67f3a2f75102e6c66ad5c2c9fea`  
		Last Modified: Fri, 26 Mar 2021 07:32:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6babb9ddf86e2a2a920201a02dc57aea8f04a9ee5ecd030a2c391bfc512823`  
		Last Modified: Fri, 26 Mar 2021 07:32:31 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:44d2e0f871f20a8c0f8cf57de6c0f0d1c9359ab15373c9c41ace02fe83198a58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9580427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc58d7f5eab2b09832550dd932e01aa25449c59f97cb180e88c6354ee990e62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:03:51 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 18 Feb 2021 01:03:54 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Mar 2021 23:12:31 GMT
ENV REDIS_VERSION=5.0.12
# Tue, 02 Mar 2021 23:12:32 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Tue, 02 Mar 2021 23:12:33 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Tue, 02 Mar 2021 23:13:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 23:13:22 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 23:13:22 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 23:13:23 GMT
WORKDIR /data
# Tue, 02 Mar 2021 23:13:24 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 23:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 23:13:27 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 23:13:27 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88a7bbd2619cadecb386208833a873a1f9de5cdee06b9d84c3dc85bf5e65087`  
		Last Modified: Thu, 18 Feb 2021 01:07:54 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f54785cfc942f98829baaec59c9cd1d970bef0aba7fc1479e88bff347e0e6a`  
		Last Modified: Thu, 18 Feb 2021 01:07:54 GMT  
		Size: 388.2 KB (388166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712e4c8cc657a4a63458b5cf8bf31b40e63c8407d867aad12b7d9ee086569601`  
		Last Modified: Tue, 02 Mar 2021 23:14:23 GMT  
		Size: 6.6 MB (6568416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178bfeb017a24500bbeee2c593ef4b3a8d2c6943ae73083f75504c79a0784479`  
		Last Modified: Tue, 02 Mar 2021 23:14:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427041b95ce5b24f7ddd258a295c53c3cc5179eeb55b5408d5280bf3f75eb389`  
		Last Modified: Tue, 02 Mar 2021 23:14:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:4416f952744ec8adfd743e48568fa004e1fbd91e09c897683081b29b8bddcde7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9273250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d47dfd9bb0303f9890f2d67aa2fae3f51297147bf80990f19f2abba85b5d647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 25 Mar 2021 22:05:53 GMT
ADD file:44ef6cff6e7d37a67c5846eb792fec65025702c00c56ff96801ac79bf81b0cc3 in / 
# Thu, 25 Mar 2021 22:05:55 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 04:37:04 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 26 Mar 2021 04:37:09 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 26 Mar 2021 04:41:29 GMT
ENV REDIS_VERSION=5.0.12
# Fri, 26 Mar 2021 04:41:30 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Fri, 26 Mar 2021 04:41:32 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Fri, 26 Mar 2021 04:42:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 26 Mar 2021 04:42:42 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 26 Mar 2021 04:42:43 GMT
VOLUME [/data]
# Fri, 26 Mar 2021 04:42:44 GMT
WORKDIR /data
# Fri, 26 Mar 2021 04:42:45 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 26 Mar 2021 04:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 04:42:47 GMT
EXPOSE 6379
# Fri, 26 Mar 2021 04:42:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6c1162af251f0d5ab4945f8506f3265b86d0a03cda37f703c2446a71a233bc20`  
		Last Modified: Thu, 25 Mar 2021 22:07:21 GMT  
		Size: 2.4 MB (2423999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8008a024110da1be37228c82d5cae76c128bdbba5e3ac9bdc7d5fff753270b5`  
		Last Modified: Fri, 26 Mar 2021 04:43:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405f26c9da7b6bdd5207e792da985e8d18029878fbbf57d2ea63db83fe2e2312`  
		Last Modified: Fri, 26 Mar 2021 04:43:31 GMT  
		Size: 383.1 KB (383056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606e72bc2da2d17d68e4ed39bec5e43b4ce950b2f1b4cf9f028dbcac3da43d53`  
		Last Modified: Fri, 26 Mar 2021 04:44:08 GMT  
		Size: 6.5 MB (6464387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba27f3d9cbca4842da45a9f09de70947f9187c05ee591aca3db30c8c1e840838`  
		Last Modified: Fri, 26 Mar 2021 04:44:06 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747f84ece964877f339c56922d54face5564b05a0eab52f121c86d553bcc614d`  
		Last Modified: Fri, 26 Mar 2021 04:44:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:ffc3863c63983732b7019a88de9b2a3276109201ba3cf43ff17bda4cd0d5ee0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9762313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80aac1746ec9c7607e74dcc7fcbfa1845dddacc8d4aa3154ba3404099a34cb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:37:00 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 18 Feb 2021 01:37:03 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Mar 2021 22:56:00 GMT
ENV REDIS_VERSION=5.0.12
# Tue, 02 Mar 2021 22:56:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Tue, 02 Mar 2021 22:56:01 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Tue, 02 Mar 2021 22:56:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 22:56:54 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 22:56:55 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 22:56:56 GMT
WORKDIR /data
# Tue, 02 Mar 2021 22:56:57 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 22:56:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 22:56:58 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 22:56:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d54d284a9344f4164841804b15309e454bbb02de1f717cd8f60062f8cbf29b9`  
		Last Modified: Thu, 18 Feb 2021 01:42:06 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c12e0e8854e7f214974b4d2386f0311360923f59a111788b15e5caed495126`  
		Last Modified: Thu, 18 Feb 2021 01:42:06 GMT  
		Size: 386.0 KB (385990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31654a959c009c06343e5cbbcc2f13522a7424902eb59ceda631ede7ce7055`  
		Last Modified: Tue, 02 Mar 2021 22:58:56 GMT  
		Size: 6.7 MB (6662945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0119680dc6eb73390ee5623ecca1146e1c630bfae797bcbeb6c663349dd624a6`  
		Last Modified: Tue, 02 Mar 2021 22:58:54 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d452947f15b7bcff64247a49777869c8f3ea3bb5a907fd43dc6f7bcd7a72d2`  
		Last Modified: Tue, 02 Mar 2021 22:58:54 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; 386

```console
$ docker pull redis@sha256:ef5addcbab9a689479dded8ade06ddfc3a2e3b6d442704a97ac6fef833065d80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c2510b65797f434d64f2aff061d6bb3dfc554c934bf250c983a57efe8c6f04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 21:36:11 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 12 Mar 2021 21:36:14 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 12 Mar 2021 21:43:01 GMT
ENV REDIS_VERSION=5.0.12
# Fri, 12 Mar 2021 21:43:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Fri, 12 Mar 2021 21:43:02 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Fri, 12 Mar 2021 21:44:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 12 Mar 2021 21:44:11 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 12 Mar 2021 21:44:11 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 21:44:11 GMT
WORKDIR /data
# Fri, 12 Mar 2021 21:44:11 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 12 Mar 2021 21:44:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Mar 2021 21:44:12 GMT
EXPOSE 6379
# Fri, 12 Mar 2021 21:44:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5f2bcb6560a0a6504a0c632b2490a3cc80368ddcd8eb5882098c35bfcf980f`  
		Last Modified: Fri, 12 Mar 2021 21:46:24 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417291f8fd42e2159995730d9a0a4d66bc930047b4edc184afac499261b9897`  
		Last Modified: Fri, 12 Mar 2021 21:46:24 GMT  
		Size: 390.6 KB (390562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2c10e8015282184ded473e5430d5aebd7b076cd0fbaf3f3916160269b5c6c2`  
		Last Modified: Fri, 12 Mar 2021 21:48:15 GMT  
		Size: 6.4 MB (6360304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ef7aa57c87988cbd8a15b44459d69fd63fff2ceecdab9123457af404d999ff`  
		Last Modified: Fri, 12 Mar 2021 21:48:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ded2c5aec62410c3e73b695f02c10cf1d468e76a3f7ece8edb000677fbad562`  
		Last Modified: Fri, 12 Mar 2021 21:48:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:6e8390946b0128dba3c091800570dbd80b72de50362ba498e4f42f2f8c1aa303
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10325072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd77db11836f7bc1957386a6bc4bd90c96d1e55cb9b4eb285a0de3386346de3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 25 Mar 2021 22:22:28 GMT
ADD file:f91f8e0aa646cb847f6e210056280f9332382ad2f8d6a8839fd9aa69b81c4a2a in / 
# Thu, 25 Mar 2021 22:22:30 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:37:38 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 26 Mar 2021 05:37:46 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 26 Mar 2021 05:42:27 GMT
ENV REDIS_VERSION=5.0.12
# Fri, 26 Mar 2021 05:42:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Fri, 26 Mar 2021 05:42:46 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Fri, 26 Mar 2021 05:43:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 26 Mar 2021 05:43:55 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 26 Mar 2021 05:43:57 GMT
VOLUME [/data]
# Fri, 26 Mar 2021 05:44:00 GMT
WORKDIR /data
# Fri, 26 Mar 2021 05:44:02 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 26 Mar 2021 05:44:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:44:11 GMT
EXPOSE 6379
# Fri, 26 Mar 2021 05:44:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f3b2866c25f0a9167af050d646a7a740ccc88d46e068c90ff28a5c2ec2ee0030`  
		Last Modified: Thu, 25 Mar 2021 22:24:08 GMT  
		Size: 2.8 MB (2813115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cda6a271137a8e5ee39c14f51c7ba99e2928ab620dd5334e9929371adb93163`  
		Last Modified: Fri, 26 Mar 2021 05:45:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dacc5116c5cde4aa4a3bb20faffd92a34cd5a04d3c63f34cb5ff14833ffa283`  
		Last Modified: Fri, 26 Mar 2021 05:45:06 GMT  
		Size: 390.7 KB (390718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c71744c7e47144ad0c7533a0627f7bb99f75d7ee77ee47119d783729b0bbd02`  
		Last Modified: Fri, 26 Mar 2021 05:45:59 GMT  
		Size: 7.1 MB (7119430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651634f603cfdd36bd6835eed50e05090dae09fb7d2085a6ca97772ae2edea77`  
		Last Modified: Fri, 26 Mar 2021 05:45:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5de9b14130ea630a92bdfd63a601298e63e4368f80fb90e5ccbf572c66dc4b`  
		Last Modified: Fri, 26 Mar 2021 05:45:55 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; s390x

```console
$ docker pull redis@sha256:9219dbca4e45ebada8401e79323bf6fb1f9de9e2f377c8fbaf7fc07b7723ab1c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9933818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7737e444013b03a0be02b855b6074a676dc563520a560254e529304fb054cfc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:34 GMT
ADD file:44e2c7cd992fc98df702bef7022e0f8c4ee86312c311ab5ae185fd5fc878edf9 in / 
# Thu, 25 Mar 2021 22:41:34 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:58:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 26 Mar 2021 07:58:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 26 Mar 2021 08:00:50 GMT
ENV REDIS_VERSION=5.0.12
# Fri, 26 Mar 2021 08:00:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Fri, 26 Mar 2021 08:00:51 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Fri, 26 Mar 2021 08:01:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 26 Mar 2021 08:01:47 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 26 Mar 2021 08:01:47 GMT
VOLUME [/data]
# Fri, 26 Mar 2021 08:01:48 GMT
WORKDIR /data
# Fri, 26 Mar 2021 08:01:48 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 26 Mar 2021 08:01:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:01:49 GMT
EXPOSE 6379
# Fri, 26 Mar 2021 08:01:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a266c0a9554add02ea09a46b8584cb36b7f606b7b4398b9ad7369f899f8360df`  
		Last Modified: Thu, 25 Mar 2021 22:42:07 GMT  
		Size: 2.6 MB (2602387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc26935d3ee732cbc8b87679a8f53b1c4728ff7a2e13a53997b026320d5e0077`  
		Last Modified: Fri, 26 Mar 2021 08:02:30 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685bfa752765525c83f0e46eae8302101e7e24ec00bc8b77357db28ce74b711b`  
		Last Modified: Fri, 26 Mar 2021 08:02:30 GMT  
		Size: 388.8 KB (388813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8163f045906e37c54a0264f306669f72e8f678bdfb1b77f78eccaab58a3a718`  
		Last Modified: Fri, 26 Mar 2021 08:02:59 GMT  
		Size: 6.9 MB (6940814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e90b61a010cca162dbcd0299ca74f10d573a05c8b626e277ab157e788abdc9`  
		Last Modified: Fri, 26 Mar 2021 08:03:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a4947aa405c3bcca80a201416512764f90373380ce8a9812d19b348d853240`  
		Last Modified: Fri, 26 Mar 2021 08:02:59 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
