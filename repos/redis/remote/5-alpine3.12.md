## `redis:5-alpine3.12`

```console
$ docker pull redis@sha256:94effe54dcaa744d51e03da51bf5f7f09e9916cca6dd57d6909f1c1cb01615d9
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

### `redis:5-alpine3.12` - linux; amd64

```console
$ docker pull redis@sha256:f89af1f9cca12e0234fcb5573bd1c2ea9fd4560888ad19d3ac2ff661facc7f42
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9961161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58084f18c7ec51ec5c9d1c29d18594d4c6dd3b1bde946d56d12faf905d4d4f4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2020 22:33:29 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 04 Jun 2020 22:33:30 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 04 Jun 2020 22:34:52 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 04 Jun 2020 22:34:52 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 04 Jun 2020 22:34:52 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 04 Jun 2020 22:35:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 04 Jun 2020 22:35:47 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 04 Jun 2020 22:35:47 GMT
VOLUME [/data]
# Thu, 04 Jun 2020 22:35:47 GMT
WORKDIR /data
# Thu, 04 Jun 2020 22:35:48 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 04 Jun 2020 22:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2020 22:35:48 GMT
EXPOSE 6379
# Thu, 04 Jun 2020 22:35:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8c029ceab510ffd36b89e8ddb97a446ab5700dd954eeecd02e500e6dec4852`  
		Last Modified: Thu, 04 Jun 2020 22:36:07 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e983a1eb737a9b9ab5e8c2846e18b0cda41703c68bc7e47a8482b4011a78592c`  
		Last Modified: Thu, 04 Jun 2020 22:36:07 GMT  
		Size: 380.7 KB (380655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a292a38549c2accd5fcbbd35bd4ad3ffd0dc47f05a883d1c970b9f86f0f012`  
		Last Modified: Thu, 04 Jun 2020 22:36:21 GMT  
		Size: 6.8 MB (6781225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba181475a1006d8e95db11aed65b38ca8b81da9160794c35d5c700098763e413`  
		Last Modified: Thu, 04 Jun 2020 22:36:19 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6445b5139fd80ee4500f947ca2e0ee447b9d0f688adfd059e59c5f274d0882ff`  
		Last Modified: Thu, 04 Jun 2020 22:36:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.12` - linux; arm variant v6

```console
$ docker pull redis@sha256:19d6d6e5e2dcc40601b70227b4c037336cf27a5f47d198871a8c4ee7b2ed9571
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9679123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddc5a0bc86c032008a5f15ff114fb0a3e86c6923adb6d17bf9b7ad2f286568a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2020 22:55:15 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 04 Jun 2020 22:55:18 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 04 Jun 2020 22:56:33 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 04 Jun 2020 22:56:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 04 Jun 2020 22:56:35 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 04 Jun 2020 22:57:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 04 Jun 2020 22:57:26 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 04 Jun 2020 22:57:27 GMT
VOLUME [/data]
# Thu, 04 Jun 2020 22:57:27 GMT
WORKDIR /data
# Thu, 04 Jun 2020 22:57:28 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 04 Jun 2020 22:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2020 22:57:29 GMT
EXPOSE 6379
# Thu, 04 Jun 2020 22:57:30 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2491f7cfcf9c696e17ac4e1826543b0841d1a6d4067364396768b07a5ed10d2d`  
		Last Modified: Thu, 04 Jun 2020 22:57:54 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dc1c58292fd74a4a2f0afcf684683f24d2c84aff9c8e60f1b79ab451e15c19`  
		Last Modified: Thu, 04 Jun 2020 22:57:54 GMT  
		Size: 384.0 KB (384009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd33b92b2a9638858a2242ee7e1e366f4edf1df7ab769ff2b989acf00167516`  
		Last Modified: Thu, 04 Jun 2020 22:58:10 GMT  
		Size: 6.7 MB (6690026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f97b767ea89c828052b7febf5099b9ae60596b0d440060768a93f23909e823`  
		Last Modified: Thu, 04 Jun 2020 22:58:07 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b241e145c2b25c9237d5a8eccfd50391e914068ba73356af1beb7925ce88ef7`  
		Last Modified: Thu, 04 Jun 2020 22:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.12` - linux; arm variant v7

```console
$ docker pull redis@sha256:da7cc995e840e67492d93467ee5df5b174bec6317a370d9557ef774f5a6f8a21
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9358427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d885ef0774c10504c930e1f1f4e9f80dd6b82f4a649cf352b8cc323a8f77f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2020 21:58:41 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 04 Jun 2020 21:58:44 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 04 Jun 2020 21:59:52 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 04 Jun 2020 21:59:53 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 04 Jun 2020 21:59:53 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 04 Jun 2020 22:00:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 04 Jun 2020 22:00:38 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 04 Jun 2020 22:00:39 GMT
VOLUME [/data]
# Thu, 04 Jun 2020 22:00:40 GMT
WORKDIR /data
# Thu, 04 Jun 2020 22:00:40 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 04 Jun 2020 22:00:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2020 22:00:42 GMT
EXPOSE 6379
# Thu, 04 Jun 2020 22:00:42 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e032461d169a86565d092c6a802fca065f93a26a09f8863354d32847f9e3ff`  
		Last Modified: Thu, 04 Jun 2020 22:01:06 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b3deaa50a54fd0aba551155315c34af4ebfcd8f651178f1992540a5f0a024a`  
		Last Modified: Thu, 04 Jun 2020 22:01:08 GMT  
		Size: 377.6 KB (377597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0f170bbb5bc8f19403ba910f50e610f895d431a66cc5a6a0e7a98e3da60645`  
		Last Modified: Thu, 04 Jun 2020 22:01:24 GMT  
		Size: 6.6 MB (6572263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9028f2f1172749c4e263b5389713c51ff35159555b6e6723764d73ade19a2a`  
		Last Modified: Thu, 04 Jun 2020 22:01:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1b803f8fe09f15cf35e5a65787c862b81ea98908fb811837141f111c929ddc`  
		Last Modified: Thu, 04 Jun 2020 22:01:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:bf284c4886f21a4a210a89c4b52d3a87bf90131479e5c78b63795b4d4f256415
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9881842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76b2cfd2fd761d0f1afda62c2b2311e88a27417cbe2f0770107f8d0fed64b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2020 22:52:14 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 04 Jun 2020 22:52:17 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 04 Jun 2020 22:53:37 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 04 Jun 2020 22:53:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 04 Jun 2020 22:53:38 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 04 Jun 2020 22:54:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 04 Jun 2020 22:54:26 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 04 Jun 2020 22:54:27 GMT
VOLUME [/data]
# Thu, 04 Jun 2020 22:54:28 GMT
WORKDIR /data
# Thu, 04 Jun 2020 22:54:28 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 04 Jun 2020 22:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2020 22:54:30 GMT
EXPOSE 6379
# Thu, 04 Jun 2020 22:54:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ce967624268d2fc70fda2e1a83da9d436c27153f185bdd30342587b2456a8c`  
		Last Modified: Thu, 04 Jun 2020 22:55:00 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfc97b74d7061059d7d0ea2b506592ca4d39cf2462555b9d96de62bbdacb419`  
		Last Modified: Thu, 04 Jun 2020 22:55:00 GMT  
		Size: 383.1 KB (383077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facd182dc880fe9c1127319785102cc6a806b64f48d7b926d33d888d9123e483`  
		Last Modified: Thu, 04 Jun 2020 22:55:19 GMT  
		Size: 6.8 MB (6788997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf18580581ce45371c50e4e8fda8b77077a12ddeebb23aa4cc2f06dd575955c`  
		Last Modified: Thu, 04 Jun 2020 22:55:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a304a10077bf9dba745f718d34b04c621f91f0c2f020923108dd6568df63c1ac`  
		Last Modified: Thu, 04 Jun 2020 22:55:17 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.12` - linux; 386

```console
$ docker pull redis@sha256:d3cfbef63e70b642d6be4305dadce46623e5263935e15fd910dae28321961483
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9672141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4068fb25a95825449ba09bc7b15b9111b785e335dac1bf3b217626f893bda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 29 May 2020 21:38:33 GMT
ADD file:5624441d97aca5eeb82a582941efc3586397098b8391227a9040ebe434cc1d6b in / 
# Fri, 29 May 2020 21:38:33 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2020 22:44:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 04 Jun 2020 22:44:19 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 04 Jun 2020 22:45:51 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 04 Jun 2020 22:45:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 04 Jun 2020 22:45:51 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 04 Jun 2020 22:46:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 04 Jun 2020 22:46:58 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 04 Jun 2020 22:46:58 GMT
VOLUME [/data]
# Thu, 04 Jun 2020 22:46:59 GMT
WORKDIR /data
# Thu, 04 Jun 2020 22:46:59 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 04 Jun 2020 22:46:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2020 22:46:59 GMT
EXPOSE 6379
# Thu, 04 Jun 2020 22:46:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0625b4155e2a59f647ece47c0cd77ed3196b1f84454fa64ce80cad90e2b9b79e`  
		Last Modified: Fri, 29 May 2020 21:38:53 GMT  
		Size: 2.8 MB (2792298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b8d7bee24f7032c92603ba89a235d5945514d906c4848a75669b0f787ab8`  
		Last Modified: Thu, 04 Jun 2020 22:47:17 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca4f94d24ace225a77b0d0ba2ee230994a7f23f01bc896f54dc8ea152dbdfd9`  
		Last Modified: Thu, 04 Jun 2020 22:47:17 GMT  
		Size: 386.2 KB (386181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c439eca7b80f61d1b6b083b5841556a3aa1b82c6dfd7fd113025bdbf59af51a`  
		Last Modified: Thu, 04 Jun 2020 22:47:29 GMT  
		Size: 6.5 MB (6491923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fc27b02e152ffe83cba968600e4c88e9c7591fe88843cea2ce4dece087d807`  
		Last Modified: Thu, 04 Jun 2020 22:47:28 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e165dd1724bd66295997897e49bb2351859f5f7a469dad10a47cd8874908aed6`  
		Last Modified: Thu, 04 Jun 2020 22:47:27 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.12` - linux; ppc64le

```console
$ docker pull redis@sha256:92eb52d3013607e230097ff6776539d2bfb5507501ed1e9c37dc73eea9b200fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10455085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717dc521f8171daecf83363a08d675d5b3a1fb0f95c502b36f11f48750417928`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2020 22:32:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 04 Jun 2020 22:32:53 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 04 Jun 2020 22:34:55 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 04 Jun 2020 22:34:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 04 Jun 2020 22:35:00 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 04 Jun 2020 22:36:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 04 Jun 2020 22:36:16 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 04 Jun 2020 22:36:20 GMT
VOLUME [/data]
# Thu, 04 Jun 2020 22:36:30 GMT
WORKDIR /data
# Thu, 04 Jun 2020 22:36:32 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 04 Jun 2020 22:36:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2020 22:36:48 GMT
EXPOSE 6379
# Thu, 04 Jun 2020 22:36:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a4eed06b46f74c11d91aa424485bad52c09b5607c232345340403d82d43992`  
		Last Modified: Thu, 04 Jun 2020 22:37:30 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705f70508e8f57ad781a7cbe3d67807948e3219d2118cf0c0f191ed66345d1d3`  
		Last Modified: Thu, 04 Jun 2020 22:37:31 GMT  
		Size: 387.6 KB (387630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c1413d09ebb889e5b71d9b5c18cdff851d598143b51194e019af5231908710`  
		Last Modified: Thu, 04 Jun 2020 22:38:01 GMT  
		Size: 7.3 MB (7260445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c835a90e7cda0a21c7b9ec990728109ffe41cc8f18fd1114f538d3912de0603`  
		Last Modified: Thu, 04 Jun 2020 22:37:57 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd345bbc6b84a46a363da2b49c215407fc2e8755120a54974dae592474b786f`  
		Last Modified: Thu, 04 Jun 2020 22:37:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.12` - linux; s390x

```console
$ docker pull redis@sha256:80eeb37e5d9e335630b704d94b5a2bf3e8116183b28d90ec769a26e68c937cb2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9969998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4124586c003f37fc8a301cf55338a9b142b3ee06cd665f62f6fd9e20a2f3cc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2020 22:49:22 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 04 Jun 2020 22:49:23 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 04 Jun 2020 22:50:09 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 04 Jun 2020 22:50:09 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 04 Jun 2020 22:50:09 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 04 Jun 2020 22:50:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 04 Jun 2020 22:50:39 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 04 Jun 2020 22:50:39 GMT
VOLUME [/data]
# Thu, 04 Jun 2020 22:50:40 GMT
WORKDIR /data
# Thu, 04 Jun 2020 22:50:40 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 04 Jun 2020 22:50:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2020 22:50:40 GMT
EXPOSE 6379
# Thu, 04 Jun 2020 22:50:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c338feeb97fe0a2fb1ad44e709e15721daf32f3607235e92e8c6189725da76`  
		Last Modified: Thu, 04 Jun 2020 22:50:55 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e4b07b0ef1066cf476f86bb29ccfc959007a13fed6acef2b2b9ea50b112945`  
		Last Modified: Thu, 04 Jun 2020 22:50:55 GMT  
		Size: 385.5 KB (385498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5ac190aa9a74f6d6465a0809c77c6681281ea9e68b72b994fdb44c58c0005e`  
		Last Modified: Thu, 04 Jun 2020 22:51:12 GMT  
		Size: 7.0 MB (7016507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8e4623349e54480c390abf4f21010545865f0629286fdde4681b4fbc8919c7`  
		Last Modified: Thu, 04 Jun 2020 22:51:16 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba857c38bd1094f5c4f84e600769d68551e99509a50b295ccb625b5d0a5890`  
		Last Modified: Thu, 04 Jun 2020 22:51:10 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
