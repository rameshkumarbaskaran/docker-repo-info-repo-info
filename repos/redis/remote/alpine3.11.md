## `redis:alpine3.11`

```console
$ docker pull redis@sha256:a508ce334f95bb8cf6e28481a5cde486db9f449a7ae018c43fdace1a9f0c0942
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

### `redis:alpine3.11` - linux; amd64

```console
$ docker pull redis@sha256:9e0055667011653cd66fffc72a9f37353fe84f83d7c14f29b942487de0b0537a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9986610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca8e389506554d8240ff1e33512fb929d7d8b4f09f2ba0176e7b55e1ea11afc`
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
# Tue, 24 Dec 2019 20:17:25 GMT
ENV REDIS_VERSION=5.0.7
# Tue, 24 Dec 2019 20:17:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.7.tar.gz
# Tue, 24 Dec 2019 20:17:26 GMT
ENV REDIS_DOWNLOAD_SHA=61db74eabf6801f057fd24b590232f2f337d422280fd19486eca03be87d3a82b
# Tue, 24 Dec 2019 20:19:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:19:19 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:19:20 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:19:20 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:19:20 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:19:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:19:21 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:19:21 GMT
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
	-	`sha256:420797c178a18c5b1f231e0cb51377454b27ddc681b73393d3f5fa0b6db5107f`  
		Last Modified: Tue, 24 Dec 2019 20:22:40 GMT  
		Size: 6.8 MB (6780539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814f7f126799a52c87d694861f3db53858068340fc1f9b83bcf1de71c8a72a27`  
		Last Modified: Tue, 24 Dec 2019 20:22:38 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20d63e017cd704ee0d70157d1ac6b1ad061a9e21c762c7bc2a0a7e6fc9fd936`  
		Last Modified: Tue, 24 Dec 2019 20:22:38 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; arm variant v6

```console
$ docker pull redis@sha256:7582833c3877baf876a50f3d52fc621d403cd1253fed8418a8b10079f8fe4fb9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9715345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a361511965e1f968c444f194bd068ba0e7813d2d1bd5f5c28a567c7a92e513`
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
# Tue, 24 Dec 2019 20:08:15 GMT
ENV REDIS_VERSION=5.0.7
# Tue, 24 Dec 2019 20:08:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.7.tar.gz
# Tue, 24 Dec 2019 20:08:17 GMT
ENV REDIS_DOWNLOAD_SHA=61db74eabf6801f057fd24b590232f2f337d422280fd19486eca03be87d3a82b
# Tue, 24 Dec 2019 20:09:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:09:08 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:09:08 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:09:09 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:09:09 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:09:10 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:09:11 GMT
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
	-	`sha256:4808aaaea53577ef8e1928e31af91fc6aa473859c4e9c8ff3ca1c9edd625f3ba`  
		Last Modified: Tue, 24 Dec 2019 20:10:29 GMT  
		Size: 6.7 MB (6695726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731dd8a691a320f3d4c04ca1d185423d9c73e264b94b5322f1639853110615c0`  
		Last Modified: Tue, 24 Dec 2019 20:10:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8079d1690ee8b955efbcd3e542e12acfb4a4eda87f389d9a3c64a08fde64041f`  
		Last Modified: Tue, 24 Dec 2019 20:10:27 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:442604c5aa360b5ee46317dab201e195e0a233902654a075e9a0d4aba16a5887
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9389053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aedca95d5b2ad5dc4c6e186d161773cd6f5eb4372a36b2bde61ac8baf3be32`
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
# Tue, 24 Dec 2019 20:46:18 GMT
ENV REDIS_VERSION=5.0.7
# Tue, 24 Dec 2019 20:46:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.7.tar.gz
# Tue, 24 Dec 2019 20:46:20 GMT
ENV REDIS_DOWNLOAD_SHA=61db74eabf6801f057fd24b590232f2f337d422280fd19486eca03be87d3a82b
# Tue, 24 Dec 2019 20:47:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:47:09 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:47:10 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:47:11 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:47:13 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:47:15 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:47:17 GMT
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
	-	`sha256:3c05f0589ae59d45898095ef9fb1638757ed3071cfb19a4b1dec94949f1ef147`  
		Last Modified: Tue, 24 Dec 2019 20:48:47 GMT  
		Size: 6.6 MB (6570781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d42730ce12271dd90762b981bb3e14ecc09443a6aaaaf19f9e4d74379e9e3f`  
		Last Modified: Tue, 24 Dec 2019 20:48:45 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312229ed05ffde95cd3b3b162ca066ed066564753d4934096de0b74ca4ec8a5f`  
		Last Modified: Tue, 24 Dec 2019 20:48:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fadefda20e4003d810e9a3e7d3c03bc8fce983e36fff71d7a1bef51fbe996619
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b2417955f7e35145b7353b19bc9427737453a22abbf64da66404b75a52a358`
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
# Tue, 24 Dec 2019 21:38:02 GMT
ENV REDIS_VERSION=5.0.7
# Tue, 24 Dec 2019 21:38:03 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.7.tar.gz
# Tue, 24 Dec 2019 21:38:03 GMT
ENV REDIS_DOWNLOAD_SHA=61db74eabf6801f057fd24b590232f2f337d422280fd19486eca03be87d3a82b
# Tue, 24 Dec 2019 21:38:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 21:38:51 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 21:38:52 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 21:38:52 GMT
WORKDIR /data
# Tue, 24 Dec 2019 21:38:53 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 21:38:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 21:38:54 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 21:38:55 GMT
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
	-	`sha256:b1c68470a7644a55bb0d5b44ac16194be4cf5ea167992b7c4d376da39dd18c64`  
		Last Modified: Tue, 24 Dec 2019 21:40:24 GMT  
		Size: 6.8 MB (6787270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5b00ad2de9dddd4e93696827921eb9d683828f7e487fa210a4d8bf1bad8d3`  
		Last Modified: Tue, 24 Dec 2019 21:40:22 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7756cf57396d69eaaa51ac2ed2788b38d7c4197e10e38a160845589376ca8c3`  
		Last Modified: Tue, 24 Dec 2019 21:40:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; 386

```console
$ docker pull redis@sha256:2452a22e45b5b79defe0affe3d77766429757b55f6a40490a97b47af6b22316b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9705828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585659fd45b6f4df7e9916b2940b0fb2398bfc2dd5009f0a75c73e39a5b7199d`
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
# Tue, 24 Dec 2019 22:38:37 GMT
ENV REDIS_VERSION=5.0.7
# Tue, 24 Dec 2019 22:38:38 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.7.tar.gz
# Tue, 24 Dec 2019 22:38:38 GMT
ENV REDIS_DOWNLOAD_SHA=61db74eabf6801f057fd24b590232f2f337d422280fd19486eca03be87d3a82b
# Tue, 24 Dec 2019 22:39:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 22:39:45 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 22:39:45 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 22:39:45 GMT
WORKDIR /data
# Tue, 24 Dec 2019 22:39:45 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 22:39:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 22:39:46 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 22:39:46 GMT
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
	-	`sha256:b45c9a06b3b45cb23eb46a8d791653ca63d31ef3e78a2db195ea7d2eca39b65d`  
		Last Modified: Tue, 24 Dec 2019 22:41:14 GMT  
		Size: 6.5 MB (6491029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49280b09286118a7e72ca809a3a0b0f4728fe2faa0fe876140e858c605acc416`  
		Last Modified: Tue, 24 Dec 2019 22:41:12 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1539542cd8a8c61f8d1db8e162c0f7ea11b0d662e221b1bd0112678669e28ea`  
		Last Modified: Tue, 24 Dec 2019 22:41:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; ppc64le

```console
$ docker pull redis@sha256:eb2eff1ec504a9a51b4704d44f19b586c06a14343acdefded1280ecf32a1765c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10487200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923870003f4879d36ee30b2519075c404a60e73b51aa2fbde63dbf8a203ad3e3`
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
# Tue, 24 Dec 2019 20:33:02 GMT
ENV REDIS_VERSION=5.0.7
# Tue, 24 Dec 2019 20:33:07 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.7.tar.gz
# Tue, 24 Dec 2019 20:33:14 GMT
ENV REDIS_DOWNLOAD_SHA=61db74eabf6801f057fd24b590232f2f337d422280fd19486eca03be87d3a82b
# Tue, 24 Dec 2019 20:34:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:34:35 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:34:40 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:34:46 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:34:47 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:34:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:34:55 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:35:02 GMT
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
	-	`sha256:5695f6e3fbd856381fc9835ac3bfd70a821c0ddee4b01b681411d377ac46cfed`  
		Last Modified: Tue, 24 Dec 2019 20:38:38 GMT  
		Size: 7.3 MB (7259036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24597729ef65f51ca0fa0154d08a3069094bff867f96d2dec1b7027f11249d77`  
		Last Modified: Tue, 24 Dec 2019 20:38:35 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a2a041a28421d930721a3cdc0380355ff8fa7d7b58a6b0dc84aa3fa2ba4c21`  
		Last Modified: Tue, 24 Dec 2019 20:38:35 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; s390x

```console
$ docker pull redis@sha256:a1be633cb230eb5aea38dcd68ae8c690c69d4abda3a324ca2f58ab70063ddc00
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10003937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12ddf52c988820e6fd5722ef23b8fd0e27627395b43b1f48cbe5537801351ad`
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
# Tue, 24 Dec 2019 20:41:03 GMT
ENV REDIS_VERSION=5.0.7
# Tue, 24 Dec 2019 20:41:03 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.7.tar.gz
# Tue, 24 Dec 2019 20:41:03 GMT
ENV REDIS_DOWNLOAD_SHA=61db74eabf6801f057fd24b590232f2f337d422280fd19486eca03be87d3a82b
# Tue, 24 Dec 2019 20:41:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 24 Dec 2019 20:41:32 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 24 Dec 2019 20:41:32 GMT
VOLUME [/data]
# Tue, 24 Dec 2019 20:41:32 GMT
WORKDIR /data
# Tue, 24 Dec 2019 20:41:33 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 24 Dec 2019 20:41:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Dec 2019 20:41:33 GMT
EXPOSE 6379
# Tue, 24 Dec 2019 20:41:33 GMT
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
	-	`sha256:b733e6b396407f4e97a7866288fa95b03b4fd14278470603469c38ce810267e2`  
		Last Modified: Tue, 24 Dec 2019 20:42:28 GMT  
		Size: 7.0 MB (7015247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036cc4481ddea247ff0e59d1695395a9eb754a6a653139efc928f838e3b51ceb`  
		Last Modified: Tue, 24 Dec 2019 20:42:27 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934bb4eafbf45c759b5bca9ba519f752e3f1746777a4e55cba3aa72306650739`  
		Last Modified: Tue, 24 Dec 2019 20:42:27 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
