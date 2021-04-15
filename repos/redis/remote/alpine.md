## `redis:alpine`

```console
$ docker pull redis@sha256:cd68f7db2caeff01a62bab0cdb5630e86e2a608b0aba3b988b1d13dcf3cfdedb
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

### `redis:alpine` - linux; amd64

```console
$ docker pull redis@sha256:f012233eecdc0f4bb9355fead6ff9681cd2b5aedbeb62f46677587e1540b7b3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10871887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6121e6a8ceb4af9336abf2ddbc4231026c8852d74976da779b8e4a40d56d091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:38:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 02:38:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 15 Apr 2021 02:38:21 GMT
ENV REDIS_VERSION=6.2.1
# Thu, 15 Apr 2021 02:38:21 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Thu, 15 Apr 2021 02:38:22 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Thu, 15 Apr 2021 02:40:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 15 Apr 2021 02:40:06 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Apr 2021 02:40:06 GMT
VOLUME [/data]
# Thu, 15 Apr 2021 02:40:07 GMT
WORKDIR /data
# Thu, 15 Apr 2021 02:40:07 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:40:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:40:08 GMT
EXPOSE 6379
# Thu, 15 Apr 2021 02:40:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712d301e8c43bcd4a36da8a8297d5ff7f68c3d4c3f7113244ff03675fa5e9c`  
		Last Modified: Thu, 15 Apr 2021 02:45:21 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8173c12df40f1578a7b2dfbbc0034a4fbc8ec7c870fd32b9236c2e5e1936616a`  
		Last Modified: Thu, 15 Apr 2021 02:45:22 GMT  
		Size: 384.2 KB (384200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3f2993175f936ef12c0b8b5a6601cc8a4d344bb4c8ad34407e7e0cdaf303b6`  
		Last Modified: Thu, 15 Apr 2021 02:45:23 GMT  
		Size: 7.7 MB (7673911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cc615d2d5780bb6c239aafb059e01816b77d806b4f809c571c7b141d26a351`  
		Last Modified: Thu, 15 Apr 2021 02:45:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f18c6c97e1f6bcaefa0079a7ec17da55f51483218e40cfb5262a8a67cbcfc8`  
		Last Modified: Thu, 15 Apr 2021 02:45:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:abc8ae4ce3db643256c2f4c93679764a8aca31daf47b8d4a439dd5228aa67d5e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10567752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def108e22fb5a1c5db9fe0510532edff0597353597c377cc4d61217dd518038b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 05:28:37 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 05:28:41 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 15 Apr 2021 05:28:42 GMT
ENV REDIS_VERSION=6.2.1
# Thu, 15 Apr 2021 05:28:42 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Thu, 15 Apr 2021 05:28:43 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Thu, 15 Apr 2021 05:29:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 15 Apr 2021 05:29:39 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Apr 2021 05:29:40 GMT
VOLUME [/data]
# Thu, 15 Apr 2021 05:29:41 GMT
WORKDIR /data
# Thu, 15 Apr 2021 05:29:41 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 15 Apr 2021 05:29:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 05:29:43 GMT
EXPOSE 6379
# Thu, 15 Apr 2021 05:29:44 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbbd4db84f7364693883d286974083c7239fac9aa12c281ffdb491b7804485`  
		Last Modified: Thu, 15 Apr 2021 05:32:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa1f16547fbe49258acf8ba93c392680545e5ae9dd673fae6f3d31dea09017`  
		Last Modified: Thu, 15 Apr 2021 05:32:26 GMT  
		Size: 388.2 KB (388162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf08fd93acca11b4d16bfe862e2086c4ea860263a0aeebfe3f5cd7965c28814`  
		Last Modified: Thu, 15 Apr 2021 05:32:28 GMT  
		Size: 7.6 MB (7555652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967cd828d91d0b7013310f0d1d9b462ca45cab73352414ff165cc030b1845f7a`  
		Last Modified: Thu, 15 Apr 2021 05:32:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe6402cbf2b4198112445e952da5fdad90ab8b48991e48b15a1d4b03b28448d`  
		Last Modified: Thu, 15 Apr 2021 05:32:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:2ee0d8dfaad03d7f1a0725a3a1fae9e30c6f3f492ca6605ff22510e208d6b1fd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10245264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1148992b318a1dd86ec9f8b504d84fac6d82b8a69112977bd175ab664e4c8a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 05:53:00 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 05:53:04 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 15 Apr 2021 05:53:05 GMT
ENV REDIS_VERSION=6.2.1
# Thu, 15 Apr 2021 05:53:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Thu, 15 Apr 2021 05:53:07 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Thu, 15 Apr 2021 05:54:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 15 Apr 2021 05:54:09 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Apr 2021 05:54:10 GMT
VOLUME [/data]
# Thu, 15 Apr 2021 05:54:12 GMT
WORKDIR /data
# Thu, 15 Apr 2021 05:54:13 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 15 Apr 2021 05:54:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 05:54:16 GMT
EXPOSE 6379
# Thu, 15 Apr 2021 05:54:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20589517e54a354da5d6cb4ea2d35203508b772c35d104b5003a9dd0f2a017`  
		Last Modified: Thu, 15 Apr 2021 05:57:37 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a8858422eeb975991be458833e2120b9fadbfacfb3530991f0e972c3370bb2`  
		Last Modified: Thu, 15 Apr 2021 05:57:37 GMT  
		Size: 383.0 KB (383040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2fc67e87d317e32784b4a4de48c3eb832c7f181653313d5a6cdc55703c9211`  
		Last Modified: Thu, 15 Apr 2021 05:57:40 GMT  
		Size: 7.4 MB (7436274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6c4dbe74d5ffc024d01cb02a4096622aa25d217cbd0ceb0c1485c894ec7d81`  
		Last Modified: Thu, 15 Apr 2021 05:57:37 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f35ef3a361b9eace9af648d55c06ad1098e7e581874d38eebfa543c0ce53ea`  
		Last Modified: Thu, 15 Apr 2021 05:57:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:3b44fed314fe141fa21d1b1e44afb98084ad312d5ea6e044ba054b96dcfc9f1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10779009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ec63569cf5e1b08299acaa5f7d19948d26141bd66197c625cd2ae926fdcef1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:14:24 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 07:14:28 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 15 Apr 2021 07:14:29 GMT
ENV REDIS_VERSION=6.2.1
# Thu, 15 Apr 2021 07:14:30 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Thu, 15 Apr 2021 07:14:32 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Thu, 15 Apr 2021 07:15:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 15 Apr 2021 07:15:34 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Apr 2021 07:15:35 GMT
VOLUME [/data]
# Thu, 15 Apr 2021 07:15:36 GMT
WORKDIR /data
# Thu, 15 Apr 2021 07:15:37 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 15 Apr 2021 07:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 07:15:39 GMT
EXPOSE 6379
# Thu, 15 Apr 2021 07:15:39 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f009ede80a4dfb2942ae27d15f3cd96afc249851ba83171edb51346d9e3d975`  
		Last Modified: Thu, 15 Apr 2021 07:19:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea11b4c6f734c1273155ea086da36c719ee65817775dd2a2d3c57cbd531da18`  
		Last Modified: Thu, 15 Apr 2021 07:19:25 GMT  
		Size: 386.0 KB (386003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e70addac769f3574ac241b0c9c404ab40e831926b84c22d51ba531ef5c462d8`  
		Last Modified: Thu, 15 Apr 2021 07:19:27 GMT  
		Size: 7.7 MB (7679172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b57dff54193f0dac0a8ba3701390b2c874d5483ceac6891923e2a99850590f`  
		Last Modified: Thu, 15 Apr 2021 07:19:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41196b2908262be47b7c5523dd6e15528ec49f3cf610e34b568a8b6fafe46286`  
		Last Modified: Thu, 15 Apr 2021 07:19:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:cfe61cde1388ca037ed485d09d116cd628b70747437ea1f4bc4af49b24a05d40
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10535996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81dd36f7e3fead9a3dc8b864b3cde54d8119c711ee2cc2d1bd18c98284f1a635`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:39:44 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 06:39:46 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 15 Apr 2021 06:39:46 GMT
ENV REDIS_VERSION=6.2.1
# Thu, 15 Apr 2021 06:39:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Thu, 15 Apr 2021 06:39:47 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Thu, 15 Apr 2021 06:40:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 15 Apr 2021 06:40:52 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Apr 2021 06:40:52 GMT
VOLUME [/data]
# Thu, 15 Apr 2021 06:40:52 GMT
WORKDIR /data
# Thu, 15 Apr 2021 06:40:53 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 15 Apr 2021 06:40:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 06:40:53 GMT
EXPOSE 6379
# Thu, 15 Apr 2021 06:40:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583b1dfa7a770c1329627c5050294279e947bfeba04c300716518c315d1080eb`  
		Last Modified: Thu, 15 Apr 2021 06:45:05 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e736134af79a478b22deba2ad536f80ae78c0cb383a88d66c2c1c5460fcc1a`  
		Last Modified: Thu, 15 Apr 2021 06:45:05 GMT  
		Size: 390.6 KB (390571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fafc806a2eb1b6d14b9e6cd57c21ec5f3f0c14ce824d0e88024f624bde3a0a`  
		Last Modified: Thu, 15 Apr 2021 06:45:09 GMT  
		Size: 7.3 MB (7324722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c62b0c082860cf4825d2c902ff86d1abfcc7ad30a103f6a85e45a8d3d653d4`  
		Last Modified: Thu, 15 Apr 2021 06:45:05 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f75c57bcb7f0114a99b5866de1a265ab1593bb79647f1227baf316966f81340`  
		Last Modified: Thu, 15 Apr 2021 06:45:05 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:1dd0247b03391d9e76533b96cc1bf1400082dc478e95c7f81296483d28e2ada5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11390191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbae9482c9d8d66f8d33f03568208b9eabc9348b5b7201fac8a16e989f00332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:55:53 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 07:56:17 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 15 Apr 2021 07:56:24 GMT
ENV REDIS_VERSION=6.2.1
# Thu, 15 Apr 2021 07:56:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Thu, 15 Apr 2021 07:56:36 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Thu, 15 Apr 2021 07:57:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 15 Apr 2021 07:58:05 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Apr 2021 07:58:09 GMT
VOLUME [/data]
# Thu, 15 Apr 2021 07:58:11 GMT
WORKDIR /data
# Thu, 15 Apr 2021 07:58:13 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 15 Apr 2021 07:58:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 07:58:19 GMT
EXPOSE 6379
# Thu, 15 Apr 2021 07:58:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846316a488fa621585c7f8607349cf8717e3025cda80dff5a9d73b1761f4c808`  
		Last Modified: Thu, 15 Apr 2021 08:05:10 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963ad60821f381aebcf57e783a69acea22d4bd86e88ebed8b3ce177afe64012f`  
		Last Modified: Thu, 15 Apr 2021 08:05:10 GMT  
		Size: 390.7 KB (390721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16531613e674eedd3ebbb51102baaf129bc5b68556639bee7e94a43c12423f56`  
		Last Modified: Thu, 15 Apr 2021 08:05:12 GMT  
		Size: 8.2 MB (8184512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8930ae02a296cbe0929910594665fb92de7f7e12587f2aefe877e269a6f44ea`  
		Last Modified: Thu, 15 Apr 2021 08:05:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ad3dd6c89ec10ef1a62f49dc0ff404ee37a403eab62828510e43d87ae9ca4e`  
		Last Modified: Thu, 15 Apr 2021 08:05:10 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:dd85ddec9b395ca8f2ce931363241d527f8c7714aad903c2d2e93943a782d78f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10985133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb605ea5ffd8630986b5fa7ec8b04bcdc839448c6105978d3e438090df108818`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:57:34 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 06:57:35 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 15 Apr 2021 06:57:35 GMT
ENV REDIS_VERSION=6.2.1
# Thu, 15 Apr 2021 06:57:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Thu, 15 Apr 2021 06:57:36 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Thu, 15 Apr 2021 06:58:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 15 Apr 2021 06:58:18 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Apr 2021 06:58:19 GMT
VOLUME [/data]
# Thu, 15 Apr 2021 06:58:19 GMT
WORKDIR /data
# Thu, 15 Apr 2021 06:58:19 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 15 Apr 2021 06:58:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 06:58:19 GMT
EXPOSE 6379
# Thu, 15 Apr 2021 06:58:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8301b8855bd6607f74a6f0e494262a313b941546f676be3a98ff67cb3921a975`  
		Last Modified: Thu, 15 Apr 2021 07:01:07 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e8e413247eebdfc21ae64af7664f78b06ca050ca165a1734e375c5db4ee9fd`  
		Last Modified: Thu, 15 Apr 2021 07:01:07 GMT  
		Size: 388.8 KB (388827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f53f6533064adb6dc96fcf944d238919278b1a522e6a2f06381256ee3849a7d`  
		Last Modified: Thu, 15 Apr 2021 07:01:09 GMT  
		Size: 8.0 MB (7991846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae9a5f26d9c01abecc57770ec4c9a60b520e55d3ed0ade7010e7aa1ba124f9b`  
		Last Modified: Thu, 15 Apr 2021 07:01:07 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b060461dbe79501ea5f8b41d1da42c6930091fec48f80d445c305ae35ed239b`  
		Last Modified: Thu, 15 Apr 2021 07:01:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
