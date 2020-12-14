## `redis:rc-alpine`

```console
$ docker pull redis@sha256:b7ad5fc6f4c990904a36d6ff74ec3cb078067ddc8bcccef64ab683948b0bd679
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

### `redis:rc-alpine` - linux; amd64

```console
$ docker pull redis@sha256:c4b1f7c786f5e018a1680e3dd041cf8a1340bd4f1aaa6e5fea7edc2a670aa62d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a638659286df905218ef6a8db3147ee2eb5f8694a3f4717e197d21870c7b4ec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 19:19:44 GMT
ENV REDIS_VERSION=6.0-rc4
# Fri, 24 Apr 2020 19:19:44 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc4.tar.gz
# Fri, 24 Apr 2020 19:19:44 GMT
ENV REDIS_DOWNLOAD_SHA=dac1ad1253337c06adf2af7f6ec7d2f54371e6b37b3c3d1c9d8fb4b7713d12a7
# Fri, 24 Apr 2020 19:20:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 19:20:41 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 19:20:42 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 19:20:42 GMT
WORKDIR /data
# Fri, 24 Apr 2020 19:20:42 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 19:20:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 19:20:42 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 19:20:42 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a935bf1649814549f372233704e9f95073ed008a8d0adb18da773f533ff4c8`  
		Last Modified: Fri, 24 Apr 2020 19:23:03 GMT  
		Size: 7.4 MB (7368051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23985a6095ece632e1270245f0047e9fd8ee79eaae6895eb3d2fa83c4ed74e97`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cada643a7d52e8fde081f6acec569909a85376ed18374c99aff23bc24c42d`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:c333d2da2d948e0a04e363d787e8d5b4120fc0cd26e6cc68af87e8668d13eef7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11790509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9dc854437b67712795f955b5c086170cbd3e8b3f68207779da077ea574532e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:10:34 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 05:10:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 21:54:54 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 21:54:55 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 21:54:56 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 21:55:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 21:55:50 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 21:55:51 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 21:55:52 GMT
WORKDIR /data
# Mon, 14 Dec 2020 21:55:52 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 21:55:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 21:55:53 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 21:55:55 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447a76a74c6810b07663d685dcd2f99da1fc67cf7824495b6f04910e7723f678`  
		Last Modified: Fri, 11 Dec 2020 05:13:24 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23f37f74eda655a638a407067de4a279a1536b0fa95d392a642008f7ca9504c`  
		Last Modified: Fri, 11 Dec 2020 05:13:24 GMT  
		Size: 384.9 KB (384903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8674de8b67b3f82ff8d2120ff362f91b14961e5c1fb6569f33a525ee5e8715bf`  
		Last Modified: Mon, 14 Dec 2020 21:56:34 GMT  
		Size: 8.8 MB (8801812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e3fa79db841c90d87d0cbcfa85212dbf107792fb2ff1f03788f883f05dd496`  
		Last Modified: Mon, 14 Dec 2020 21:56:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5fc7263af02fc3dea7b8a7108077485b59a8c141c620390489ed946b9cf582`  
		Last Modified: Mon, 14 Dec 2020 21:56:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:d158565119795602a490c00265f4cae5a23410237c7672dc3978cf16fec8a4f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9945548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afee444fdbf51e9b6643ed2cd90a88bafb43dcc3a500538fb25b8c6c68c25ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 08:51:37 GMT
ENV REDIS_VERSION=6.0-rc4
# Fri, 24 Apr 2020 08:51:37 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc4.tar.gz
# Fri, 24 Apr 2020 08:51:38 GMT
ENV REDIS_DOWNLOAD_SHA=dac1ad1253337c06adf2af7f6ec7d2f54371e6b37b3c3d1c9d8fb4b7713d12a7
# Fri, 24 Apr 2020 08:52:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 08:52:25 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 08:52:26 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 08:52:27 GMT
WORKDIR /data
# Fri, 24 Apr 2020 08:52:28 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 08:52:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 08:52:29 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 08:52:30 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fbe6c41a350debf44fdd39fb2ea6b0ffa8630e8ba62a375b0a6f309e2d9925`  
		Last Modified: Fri, 24 Apr 2020 08:55:18 GMT  
		Size: 7.1 MB (7121903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90b7d4d4f4493ae6e68268f56038ac514f054a4f8191eb6a924459b43c26010`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f183329c6b0d975cca1eb83833888c2e490ddb7e7d2ef7ea9f4932afa8961de1`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:47a3549b6823c0b66ea6b92373e178c0cf23d806d4b96c6660d2781fd2e0f17c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c542843cc364d1fe22a1dfd5eb0886b127699aa72b0cc4ca88eed5fc01a39d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 15:02:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 15:02:27 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 21:57:28 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 21:57:28 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 21:57:29 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 21:58:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 21:58:22 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 21:58:23 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 21:58:25 GMT
WORKDIR /data
# Mon, 14 Dec 2020 21:58:26 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 21:58:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 21:58:28 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 21:58:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644769aa9380d3217180aef39343466a8888ab65d032d49b2e0d076e1ae64439`  
		Last Modified: Fri, 11 Dec 2020 15:08:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d71757449c7064c22fec07fcdc49bb7e35eb87d73ea3bf8c27d1a905d48919d`  
		Last Modified: Fri, 11 Dec 2020 15:08:09 GMT  
		Size: 383.9 KB (383919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1679d88505042e576c9b4dd8413aba2e508da88db303e7b289039ab3864c172b`  
		Last Modified: Mon, 14 Dec 2020 21:59:50 GMT  
		Size: 9.1 MB (9073100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023b67d9d7332e51fe9aadc85f2620bd856cf9859d1294c2fb9d69511a6197b3`  
		Last Modified: Mon, 14 Dec 2020 21:59:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9da9d4a93c1ceffa9510d7f6c9406213701b241c98eb145f30f38a2fdc81344`  
		Last Modified: Mon, 14 Dec 2020 21:59:47 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; 386

```console
$ docker pull redis@sha256:01c88cd085ce96a8c0a0c9a35717df5483294d14c87c7320bdb2072c8e0e7385
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12019731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52edf933d4fdeb62bb4b3edbc9e2e4d2664e0658f368134367e23172e5286480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 21:36:53 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 21:36:54 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 21:41:03 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 21:41:04 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 21:41:04 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 21:42:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 21:42:18 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 21:42:18 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 21:42:19 GMT
WORKDIR /data
# Mon, 14 Dec 2020 21:42:19 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 21:42:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 21:42:19 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 21:42:19 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c7c02d89eb295e848e91a38659a947216b36c0341aaca883e067f6bb4e65a0`  
		Last Modified: Fri, 11 Dec 2020 21:42:12 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04935f19e0740c2dc4402dc74f1bec97b3192ebb3cfe86024468916307be56a3`  
		Last Modified: Fri, 11 Dec 2020 21:42:13 GMT  
		Size: 387.0 KB (386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdd2480b1faed5e5088097c898c0bcd9ef784935845053d2f3bb2ede68abc2f`  
		Last Modified: Mon, 14 Dec 2020 21:43:34 GMT  
		Size: 8.8 MB (8839527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e83082361a721a6c2386aafdaff184b588cccae95fcddcce97b74b359a663d`  
		Last Modified: Mon, 14 Dec 2020 21:43:32 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec81850553a4ea0b17f004854eb85fd24a1fc6dc489975de45fb9e4348cd950f`  
		Last Modified: Mon, 14 Dec 2020 21:43:31 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:cbf2feb042c10973001a2d073b15b908f7d2cf1c225ebce905a63dc77680c4af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11099878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21cb2c3c071854f2bd1116d5bc0432947e288d02cb8a767afd88ead475e5174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 09:02:16 GMT
ENV REDIS_VERSION=6.0-rc4
# Fri, 24 Apr 2020 09:02:21 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc4.tar.gz
# Fri, 24 Apr 2020 09:02:23 GMT
ENV REDIS_DOWNLOAD_SHA=dac1ad1253337c06adf2af7f6ec7d2f54371e6b37b3c3d1c9d8fb4b7713d12a7
# Fri, 24 Apr 2020 09:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 09:03:19 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 09:03:21 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 09:03:23 GMT
WORKDIR /data
# Fri, 24 Apr 2020 09:03:24 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:03:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 09:03:29 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 09:03:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fb1e8e3a92e37087c222fb0dba39c998aa32641467d7a9afc00d9545ab7008`  
		Last Modified: Fri, 24 Apr 2020 09:06:59 GMT  
		Size: 7.9 MB (7866357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402ae2b6bbc13c921284dcdaaf04c675b347980e9162b889aa4235c26e56369`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dd6bc3a454a348b1b307e55f4da0c986c64d923de13d14090c8b52e62878b2`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; s390x

```console
$ docker pull redis@sha256:ec1aabc6050e9b68f81bda9ff8ecdb07e1aa6b9f88f5fe7214465d9ec854c37b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12146474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecdeaac97b32776cffedbdd78522b7c8c6612f3f83bad3aa98b9c8494219e80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 13:58:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 13:58:35 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 21:45:55 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 21:45:55 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 21:45:56 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 21:46:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 21:46:37 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 21:46:37 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 21:46:37 GMT
WORKDIR /data
# Mon, 14 Dec 2020 21:46:38 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 21:46:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 21:46:38 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 21:46:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fd6145aff29902d4fd018025ad260fe864cbe9f06627b6964ba58e33a2aa7`  
		Last Modified: Fri, 11 Dec 2020 14:04:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732b2116381efd347a216d9f6b13848bbe0ece877b2e04b99db18bb895ef06b`  
		Last Modified: Fri, 11 Dec 2020 14:04:21 GMT  
		Size: 386.4 KB (386378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0941270b2a08de0fd0e889a435cd15e8385d77c9c309741d921fb5574cccc814`  
		Last Modified: Mon, 14 Dec 2020 21:47:54 GMT  
		Size: 9.2 MB (9192303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327e812487ec9f968b57efa27cba3049dc846ee4b0215262e3b9ee46f5916a98`  
		Last Modified: Mon, 14 Dec 2020 21:47:52 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f057f0e58900d2bff4800535692e9cb55ec157b4d4d6347eecdb32b6df30fbf`  
		Last Modified: Mon, 14 Dec 2020 21:47:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
