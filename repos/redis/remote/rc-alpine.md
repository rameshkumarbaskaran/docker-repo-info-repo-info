## `redis:rc-alpine`

```console
$ docker pull redis@sha256:c00f63b2b051e859031b3259538580d69ebb90d53c569076dfd558e2e16b2e47
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
$ docker pull redis@sha256:501ed92f59bf402793b91ed6da111652ef33cb7efdf997872784030c12fb3bff
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10482222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d5ef218b9a09d4ce973fe38f8304e2731d11a39e26e3ad56df4f9ab6c04c2d`
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
# Tue, 24 Dec 2019 20:15:01 GMT
ENV REDIS_VERSION=6.0-rc1
# Tue, 24 Dec 2019 20:15:01 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc1.tar.gz
# Tue, 24 Dec 2019 20:15:02 GMT
ENV REDIS_DOWNLOAD_SHA=2676012e2fcfe8d41e594b2ae8a05d0a050d2d84c38a0471ae5fe0143e4b0eca
# Tue, 24 Dec 2019 20:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:16:58 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:16:59 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:16:59 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:16:59 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:17:00 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:17:00 GMT
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
	-	`sha256:398e99c452e3e7bfd2ea1971bbe22c50f4ff1c70774474c4792b02242363cfc3`  
		Last Modified: Tue, 24 Dec 2019 20:22:25 GMT  
		Size: 7.3 MB (7276153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a1ade1bf791e00f31a117a76e7fe9d9308378730403ed5bf23340d25549810`  
		Last Modified: Tue, 24 Dec 2019 20:22:23 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2301f124e3b5e585fef7a60f6b0e3722952a011347048c94e1aef25d6c9360c5`  
		Last Modified: Tue, 24 Dec 2019 20:22:23 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:436b586ddabeacf384809af0ea7aae8e8a049b7dd8dd45cc0e7d0e41d8785d32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10190417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c2d825f72544f926eaedec0c5613d15c617baec01b53586edad4e8070caa67`
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
# Tue, 24 Dec 2019 20:06:36 GMT
ENV REDIS_VERSION=6.0-rc1
# Tue, 24 Dec 2019 20:06:36 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc1.tar.gz
# Tue, 24 Dec 2019 20:06:37 GMT
ENV REDIS_DOWNLOAD_SHA=2676012e2fcfe8d41e594b2ae8a05d0a050d2d84c38a0471ae5fe0143e4b0eca
# Tue, 24 Dec 2019 20:07:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:07:48 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:07:49 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:07:51 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:07:52 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:07:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:07:55 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:07:56 GMT
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
	-	`sha256:34f215b699a6f57f25b64a3b66a66fe3dfdf9ea9bb05c212ebcedbdfdf817cee`  
		Last Modified: Tue, 24 Dec 2019 20:10:15 GMT  
		Size: 7.2 MB (7170797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0c0865fe663cea52985f8bcc81d14148792771e97eb83eb921105c64681009`  
		Last Modified: Tue, 24 Dec 2019 20:10:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804d8e13ded2f29f9fc01d53f9801d72cf4d523597570da3637f59ce833f572a`  
		Last Modified: Tue, 24 Dec 2019 20:10:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:df7a1baec76b33a0cb5a0a20f69b5837e8c53196b8e681c7a74233bdc7c2eb91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9858735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ce8b5c05145e31adab94c84607de28b72a371cbe5dd0d593ac23a267877d0`
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
# Tue, 24 Dec 2019 20:44:41 GMT
ENV REDIS_VERSION=6.0-rc1
# Tue, 24 Dec 2019 20:44:43 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc1.tar.gz
# Tue, 24 Dec 2019 20:44:45 GMT
ENV REDIS_DOWNLOAD_SHA=2676012e2fcfe8d41e594b2ae8a05d0a050d2d84c38a0471ae5fe0143e4b0eca
# Tue, 24 Dec 2019 20:46:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:46:03 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:46:03 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:46:04 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:46:05 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:46:06 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:46:07 GMT
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
	-	`sha256:742ac9c452514c39f8796e882daa3279d15679241104d92b0a577193cd74b9e0`  
		Last Modified: Tue, 24 Dec 2019 20:48:33 GMT  
		Size: 7.0 MB (7040465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef88aace70206e3cdb91e9ecc05114567dff5e4239f95bc738d0c463905d77b`  
		Last Modified: Tue, 24 Dec 2019 20:48:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53577763a5f6a21f4ed0daa1818880d63e49d404a7bec1a552faccad1ff92db1`  
		Last Modified: Tue, 24 Dec 2019 20:48:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:0cb72c5226b73b1db68c76f68f0ca39a9f71e0c27f7c75ffa2cc794457ae4088
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10401104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be352c4a720dd536956b929677ce092ca603b4e4a2648d1557ea962cf066bad`
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
# Tue, 24 Dec 2019 21:36:56 GMT
ENV REDIS_VERSION=6.0-rc1
# Tue, 24 Dec 2019 21:36:56 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc1.tar.gz
# Tue, 24 Dec 2019 21:36:57 GMT
ENV REDIS_DOWNLOAD_SHA=2676012e2fcfe8d41e594b2ae8a05d0a050d2d84c38a0471ae5fe0143e4b0eca
# Tue, 24 Dec 2019 21:37:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 21:37:45 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 21:37:45 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 21:37:46 GMT
WORKDIR /data
# Tue, 24 Dec 2019 21:37:46 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 21:37:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 21:37:47 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 21:37:48 GMT
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
	-	`sha256:50d648d5beaf5784e54c404b8df783598639c13b9bf82c30de0643742f49702c`  
		Last Modified: Tue, 24 Dec 2019 21:40:10 GMT  
		Size: 7.3 MB (7275458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb0fe326a182683093eeb6af93165406f67abb5ce32959fdc7a24c1914aa6d9`  
		Last Modified: Tue, 24 Dec 2019 21:40:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c453559a3093c8d930eb8f12b297e366e44fdc37c1658fec5f67660417fb673`  
		Last Modified: Tue, 24 Dec 2019 21:40:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; 386

```console
$ docker pull redis@sha256:7daefbd0eb0a8da91b85a6ff062f9766f70b740a3d6dd6bc28dfc9bc42167286
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10171755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e1d3bcf8b9faade4722bfceb8c8bd117143997251323f6844551f5ab29b24f`
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
# Tue, 24 Dec 2019 22:37:07 GMT
ENV REDIS_VERSION=6.0-rc1
# Tue, 24 Dec 2019 22:37:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc1.tar.gz
# Tue, 24 Dec 2019 22:37:07 GMT
ENV REDIS_DOWNLOAD_SHA=2676012e2fcfe8d41e594b2ae8a05d0a050d2d84c38a0471ae5fe0143e4b0eca
# Tue, 24 Dec 2019 22:38:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 22:38:17 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 22:38:17 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 22:38:17 GMT
WORKDIR /data
# Tue, 24 Dec 2019 22:38:17 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 22:38:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:38:17 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 22:38:18 GMT
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
	-	`sha256:acec336107d19b5473976cfc9aa67fa7ee04845d58b04b172f507687c7dfb568`  
		Last Modified: Tue, 24 Dec 2019 22:41:05 GMT  
		Size: 7.0 MB (6956956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd30682d58ebe37017becdc0e574b11b28eef0d09bccdb405ae9a429c93e746`  
		Last Modified: Tue, 24 Dec 2019 22:41:04 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fb404c335287ddf19a55bcbd5c55a55e39c70e45717e0d063d9c8218386a3f`  
		Last Modified: Tue, 24 Dec 2019 22:41:04 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:6cc17821360e228b25200244e8188eea6f31dc7f26abe66612769ad877771697
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10996863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3a6264ee876a5e3c3bca4ccc8565feee5c9b9a3268a6cdd0968306657c194f`
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
# Tue, 24 Dec 2019 20:31:01 GMT
ENV REDIS_VERSION=6.0-rc1
# Tue, 24 Dec 2019 20:31:05 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc1.tar.gz
# Tue, 24 Dec 2019 20:31:09 GMT
ENV REDIS_DOWNLOAD_SHA=2676012e2fcfe8d41e594b2ae8a05d0a050d2d84c38a0471ae5fe0143e4b0eca
# Tue, 24 Dec 2019 20:32:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:32:17 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:32:22 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:32:25 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:32:27 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:32:35 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:32:38 GMT
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
	-	`sha256:2642d2be3307ab0ab3d020be73502d62d002707c985386e5ad6cf6b29c56e646`  
		Last Modified: Tue, 24 Dec 2019 20:38:05 GMT  
		Size: 7.8 MB (7768702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402cdf20e03723ab00ae1948ad2ec3e0914d5980d4256bb536d30724528aab8`  
		Last Modified: Tue, 24 Dec 2019 20:38:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f245c53e79c9a94977f523071c1e5abbd07ac87fde55043a977e4337b84c553`  
		Last Modified: Tue, 24 Dec 2019 20:38:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; s390x

```console
$ docker pull redis@sha256:4bc5830941adda736b1c1eb7d14b81b2539296c59dc461454d89a4a3c01e42a2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f125a74e017cf592be74f62fb55a8478dc3cf069eeff03c77e6e71ec0933021`
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
# Tue, 24 Dec 2019 20:40:19 GMT
ENV REDIS_VERSION=6.0-rc1
# Tue, 24 Dec 2019 20:40:19 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc1.tar.gz
# Tue, 24 Dec 2019 20:40:19 GMT
ENV REDIS_DOWNLOAD_SHA=2676012e2fcfe8d41e594b2ae8a05d0a050d2d84c38a0471ae5fe0143e4b0eca
# Tue, 24 Dec 2019 20:40:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:40:49 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:40:49 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:40:49 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:40:50 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:40:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:40:50 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:40:50 GMT
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
	-	`sha256:ba4cf5e76effe17c2f52421fba43861dba654a2a54c9442bb3bab93d62c018de`  
		Last Modified: Tue, 24 Dec 2019 20:42:19 GMT  
		Size: 7.5 MB (7535228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc52a3e8797550477ef0897360ecbb86ed45690c7c937e1b1edafc53a27ae25c`  
		Last Modified: Tue, 24 Dec 2019 20:42:17 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213ccb90a94f02ceb5ce1e6fa8738e774e3b3f84d53986579d511c1816983af3`  
		Last Modified: Tue, 24 Dec 2019 20:42:17 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
