## `redis:4-alpine3.11`

```console
$ docker pull redis@sha256:cc33d01d0c96e498284886d2afc0a5d09250334efd61dd430e5edce9b89a9a3c
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

### `redis:4-alpine3.11` - linux; amd64

```console
$ docker pull redis@sha256:65347ecba05504b315e0c719a44883f56ca47c7ccccfd39d5f34821802163cd9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7707665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ad7e35eaadbebda4636243ec7d3f4063dbb9ac334d4adcd4c7577695660be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 20:14:58 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 24 Dec 2019 20:15:01 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 24 Dec 2019 20:19:52 GMT
ENV REDIS_VERSION=4.0.14
# Tue, 24 Dec 2019 20:19:52 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Tue, 24 Dec 2019 20:19:53 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Tue, 24 Dec 2019 20:20:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:20:56 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:20:56 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:20:57 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:20:57 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:20:58 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:20:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5ff11edca67531e0937045954dac7484778b96d3e77f5a0d6056cca7f4ab90`  
		Last Modified: Tue, 24 Dec 2019 20:22:23 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fa80ee947360e5477d9d5904bdbce44e47c2f8716d1f87ecc3b7a754071db8`  
		Last Modified: Tue, 24 Dec 2019 20:22:23 GMT  
		Size: 402.6 KB (402555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c2c56e88f2361412d258d3242fd3c596cf8c5ca3dfbbf262796be6a09a6b6`  
		Last Modified: Tue, 24 Dec 2019 20:22:55 GMT  
		Size: 4.5 MB (4501593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a23f8b46bb821d5abe55db21f0b780bce87ceab69ae2ab7c87c2e75321364`  
		Last Modified: Tue, 24 Dec 2019 20:22:54 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7dcea08bcc9063d9f95ac55694aa9aff90a1316e27416f16aff1e69e044c01`  
		Last Modified: Tue, 24 Dec 2019 20:22:54 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; arm variant v6

```console
$ docker pull redis@sha256:e8839115d50032ff76bd58e7ce8a33ffa7ca0deae43d3cdab65311c6e352bfb2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515ad922a68c22700025eda7ab1fd617cbf61b1933809878a03f337ab4f73c52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 20:06:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 24 Dec 2019 20:06:35 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 24 Dec 2019 20:09:22 GMT
ENV REDIS_VERSION=4.0.14
# Tue, 24 Dec 2019 20:09:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Tue, 24 Dec 2019 20:09:24 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Tue, 24 Dec 2019 20:09:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:09:53 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:09:53 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:09:54 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:09:55 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:09:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:09:56 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:09:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6690ebdbfaabe4d222e0989fa8663a736e4d4fcb9172c9bfc7ebf5866172bf5a`  
		Last Modified: Tue, 24 Dec 2019 20:10:13 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a8fc7c7c940bf5b9b6c72b079564f927090d1ac1b8c983fc63187cd5a0ee85`  
		Last Modified: Tue, 24 Dec 2019 20:10:13 GMT  
		Size: 405.8 KB (405793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93668bafdbe2f1a4dc1c03e629567451548fff5962992012d25c9259b610c2c`  
		Last Modified: Tue, 24 Dec 2019 20:10:42 GMT  
		Size: 4.3 MB (4330775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775e6b35db11b4d128f77895fc0445361884c697675d83b78e0c2ff0211c29d6`  
		Last Modified: Tue, 24 Dec 2019 20:10:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccb567e94841b23aef60231b79803df0e66863716a6de68a6f5e1ec34e0892a`  
		Last Modified: Tue, 24 Dec 2019 20:10:42 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:e93d842644688d780f3eedd2ce5606e0d6badcde25dda249071411a4a23c3f1d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7072895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0beb90574ed8f5b83f032756482d9ad2d63d3538360e73f6995ba87cc0a84f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 20:44:33 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 24 Dec 2019 20:44:40 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 24 Dec 2019 20:47:30 GMT
ENV REDIS_VERSION=4.0.14
# Tue, 24 Dec 2019 20:47:30 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Tue, 24 Dec 2019 20:47:31 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Tue, 24 Dec 2019 20:47:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:47:58 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:47:59 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:47:59 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:48:00 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:48:01 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:48:02 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb845f4a68f07a520a518f5d1ffd397679ad8af7fa5e53d0c647f26ad5c9fd02`  
		Last Modified: Tue, 24 Dec 2019 20:48:30 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df621bbb71ea946244d3e8863368412b46b3e06c4e846a7178fb2b8efb6e17f`  
		Last Modified: Tue, 24 Dec 2019 20:48:30 GMT  
		Size: 399.8 KB (399775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96503dfbd0a2e5a1240ff06c3968bd0272acf006e54f077ab6068502bc00db02`  
		Last Modified: Tue, 24 Dec 2019 20:49:03 GMT  
		Size: 4.3 MB (4254625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12830a234e0282d1caf1ba6496b9befe748ac8638f0f79cce16509868737f9a`  
		Last Modified: Tue, 24 Dec 2019 20:49:01 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25adca6a2254292e7ec9089a87a85eb0823a6e8fb401bf81d83d2fa6fbf8aa06`  
		Last Modified: Tue, 24 Dec 2019 20:49:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fcebef0bd6272e167f689368fd5f84d5f09d2bce6214f5ef1f48f37a5ff60119
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7528415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47d9561c745a9ee7a75fd99bf80c12cc96f6253be0035fb586098f477fb5afb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 21:36:53 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 24 Dec 2019 21:36:55 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 24 Dec 2019 21:39:12 GMT
ENV REDIS_VERSION=4.0.14
# Tue, 24 Dec 2019 21:39:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Tue, 24 Dec 2019 21:39:14 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Tue, 24 Dec 2019 21:39:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 21:39:40 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 21:39:40 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 21:39:41 GMT
WORKDIR /data
# Tue, 24 Dec 2019 21:39:41 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 21:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 21:39:43 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 21:39:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e5527b2c4228c8cae1dea3684631a5b3320e665960c29c0aa4a5fce854198c`  
		Last Modified: Tue, 24 Dec 2019 21:40:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b34c2c544f18db3904a205c7d612b06f7cb3618ae089403278b5a5edcfade03`  
		Last Modified: Tue, 24 Dec 2019 21:40:08 GMT  
		Size: 404.7 KB (404658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35a093a52a2a5956abe5ccb485d14c5520747991ffe0e56e43f2982dc902e66`  
		Last Modified: Tue, 24 Dec 2019 21:40:38 GMT  
		Size: 4.4 MB (4402771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dbfa0a7289ae9751d587fd6b712240befda29e77bc93c94758d4dda53d880f`  
		Last Modified: Tue, 24 Dec 2019 21:40:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76587b0cf090cd8d90a8532cd1616ba1afa49b47c2f8022bce7f90b529050899`  
		Last Modified: Tue, 24 Dec 2019 21:40:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; 386

```console
$ docker pull redis@sha256:aa6a548a557acc45152429c1166d9de9448fc0014e0bb76c327c5a0bef5ca286
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1db7f5b592b33e019b45d0244e5f6da94835b512c1efecd04ff18662a270688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 22:37:05 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 24 Dec 2019 22:37:07 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 24 Dec 2019 22:39:56 GMT
ENV REDIS_VERSION=4.0.14
# Tue, 24 Dec 2019 22:39:56 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Tue, 24 Dec 2019 22:39:56 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Tue, 24 Dec 2019 22:40:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 22:40:32 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 22:40:32 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 22:40:32 GMT
WORKDIR /data
# Tue, 24 Dec 2019 22:40:32 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 22:40:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:40:33 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 22:40:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cbe0acfe3faf3101d7c8daddebef28303450f801a706b4b586db7490b2c11a`  
		Last Modified: Tue, 24 Dec 2019 22:41:04 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2a90697d0698d45923f3cd38872000eaf66147ef07aaf2766fe4e1982b4912`  
		Last Modified: Tue, 24 Dec 2019 22:41:04 GMT  
		Size: 407.9 KB (407911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcec8e351f2bb357bb394c72e7ba073b3759c7afd521a3b28ac830d99a4e454`  
		Last Modified: Tue, 24 Dec 2019 22:41:23 GMT  
		Size: 4.3 MB (4259159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0f1cf331cc1da0c34364211368e60cb4da4d6995a77aedf3a815b043af3f7f`  
		Last Modified: Tue, 24 Dec 2019 22:41:22 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb532cbd98f18ded327d9a53f780c595f975e074981e9cf376b8612fcebdc7e8`  
		Last Modified: Tue, 24 Dec 2019 22:41:23 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; ppc64le

```console
$ docker pull redis@sha256:ec1275eb85f6d889ea57c8b2bb7888e0f8c185604bdf88e44a7d29576fbba0ff
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7911277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2d7a8e9e56a761e278f3128b7b3530ef6d747d6f11c0deb4e4285c7fb6f303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 20:30:45 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 24 Dec 2019 20:30:57 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 24 Dec 2019 20:35:21 GMT
ENV REDIS_VERSION=4.0.14
# Tue, 24 Dec 2019 20:35:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Tue, 24 Dec 2019 20:35:29 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Tue, 24 Dec 2019 20:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:36:23 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:36:28 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:36:33 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:36:35 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:36:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:36:40 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:36:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec98a815652651227cde929032b86b4e74b97f25c96435f5f938a388ea821608`  
		Last Modified: Tue, 24 Dec 2019 20:38:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d541bbafc448828f3fe8671379551e915de8ee4752aea51ff6b90b6a89a59e5d`  
		Last Modified: Tue, 24 Dec 2019 20:38:03 GMT  
		Size: 409.9 KB (409873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187021dd83fed5fe9b60ef4d26a4cdfabdedeedbe94677782323d7a16b8e73c1`  
		Last Modified: Tue, 24 Dec 2019 20:39:20 GMT  
		Size: 4.7 MB (4683113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db15b7f3fd69caa84f8c91d9894422253be6e470c757e3a00dc1989f75d7c79`  
		Last Modified: Tue, 24 Dec 2019 20:39:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5531d04114a78ab4017c8bf61f7d176088e63fb8d1c547710db7d779f843b13`  
		Last Modified: Tue, 24 Dec 2019 20:39:18 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; s390x

```console
$ docker pull redis@sha256:97e4269b3497da188f25712a828098b088b704670ce1576ed84d52d33d87e10a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4891d5525041fc1491993fb858c6f009fcd5dceee6bc9b33251adcf82e50804d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 24 Dec 2019 20:16:56 GMT
ADD file:d26fbcd308b78da175af74382b16ee1f7a3370ab9d618b306d604d292e72c560 in / 
# Tue, 24 Dec 2019 20:16:56 GMT
CMD ["/bin/sh"]
# Tue, 24 Dec 2019 20:40:18 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 24 Dec 2019 20:40:19 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 24 Dec 2019 20:41:43 GMT
ENV REDIS_VERSION=4.0.14
# Tue, 24 Dec 2019 20:41:43 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Tue, 24 Dec 2019 20:41:43 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Tue, 24 Dec 2019 20:41:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:41:58 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:41:59 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:41:59 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:41:59 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:41:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:41:59 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:42:00 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bca389ebb9be8103bf737251d68f962104771b2f9c1fff1f7ae0207458fa4c86`  
		Last Modified: Tue, 24 Dec 2019 20:17:18 GMT  
		Size: 2.6 MB (2579591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e07ee4313a681359a7a34cb7e38cf1ab1203a05bdb0c31199de86bb63c77e2`  
		Last Modified: Tue, 24 Dec 2019 20:42:18 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8e178bc6600fcf408e03744a3727dde9be59c3b4cc3b212a2f8562dd20259d`  
		Last Modified: Tue, 24 Dec 2019 20:42:18 GMT  
		Size: 407.4 KB (407361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f53db78059f6ed8b2d12df0e5163fe07d6b14958a7da2e9c932c2c5106fc92`  
		Last Modified: Tue, 24 Dec 2019 20:42:38 GMT  
		Size: 4.6 MB (4564756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57d693ae05eefcc7f51973037665db53d07f9bea20933a4321c54a46e192347`  
		Last Modified: Tue, 24 Dec 2019 20:42:37 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f93c36de492c6ceb8a488b08646606232a3cce242ab45d897ce099c9e018d3e`  
		Last Modified: Tue, 24 Dec 2019 20:42:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
