## `redis:alpine`

```console
$ docker pull redis@sha256:d22559cc2ad62015bfdba23f342f8abfafdbaa4c02abbe0753103b7190c1d9cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redis:alpine` - linux; amd64

```console
$ docker pull redis@sha256:a954691db2c951a2b0e5de460e154e8bf3ce466c8903d4acb84a15081b38769b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18090810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246a9110fd9ec0f61475090b9077a4720a1fc2afae697b0f72b3f6706b67fd86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 15:23:15 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Fri, 10 Nov 2023 15:23:15 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Fri, 10 Nov 2023 15:23:15 GMT
ENV REDIS_VERSION=7.2.3
# Fri, 10 Nov 2023 15:23:15 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.3.tar.gz
# Fri, 10 Nov 2023 15:23:15 GMT
ENV REDIS_DOWNLOAD_SHA=3e2b196d6eb4ddb9e743088bfc2915ccbb42d40f5a8a3edd8cb69c716ec34be7
# Fri, 10 Nov 2023 15:23:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.3","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.3?os_name=alpine&os_version=3.18"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 10 Nov 2023 15:23:15 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 10 Nov 2023 15:23:15 GMT
VOLUME [/data]
# Fri, 10 Nov 2023 15:23:15 GMT
WORKDIR /data
# Fri, 10 Nov 2023 15:23:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 15:23:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Nov 2023 15:23:15 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 10 Nov 2023 15:23:15 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f150590280ce9d2d46fb8de9dce98b90b1d2856f7daa9aaaa0b31c728712c52c`  
		Last Modified: Thu, 16 Nov 2023 01:21:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28642122f09bbe4d5d837efa60ad0d31d8f0a3f24a9dfac520bd6d9b0313114`  
		Last Modified: Thu, 16 Nov 2023 01:21:29 GMT  
		Size: 347.4 KB (347376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02f0386730cac29f016dda3497771a836906e8367f09e1523d0a7317dc6253`  
		Last Modified: Thu, 16 Nov 2023 01:21:29 GMT  
		Size: 14.3 MB (14339527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c996777deab92574a4edd42b7c5982919e8d185072a5bfbfdeb7b886b6d710`  
		Last Modified: Thu, 16 Nov 2023 01:21:29 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce1e561adcd923e8603a5039ef80b72e33fae0b1113194359ce7940312d8a4c`  
		Last Modified: Thu, 16 Nov 2023 01:21:30 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:b38683d053cc6495191456bf632fd060239f69cd25c4881a87a696800d545627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.9 KB (718932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16c1f0b4c508da14770e6043eaa84a336a87a9308a8b356d2d553e992ee69f9`

```dockerfile
```

-	Layers:
	-	`sha256:cd7e27764a9f93b97cef7756639d92a616853435262e689998204ca605e6be30`  
		Last Modified: Thu, 16 Nov 2023 01:21:29 GMT  
		Size: 691.4 KB (691397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aedacb7113370e60756d6b0b76db64b26b6f186da374bde7cb61c37cda923f0f`  
		Last Modified: Thu, 16 Nov 2023 01:21:29 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:e87437dd1c459cb35eb52442dd6e9ed6df6ea4ffd1800e675c7dbcdc9811a9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17662493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374756ce87b077d2eea2eb26573b76d041c31d2d4d5c406a85a96cfcbbb41652`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_VERSION=7.2.3
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.3.tar.gz
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_SHA=3e2b196d6eb4ddb9e743088bfc2915ccbb42d40f5a8a3edd8cb69c716ec34be7
# Wed, 01 Nov 2023 16:56:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
VOLUME [/data]
# Wed, 01 Nov 2023 16:56:23 GMT
WORKDIR /data
# Wed, 01 Nov 2023 16:56:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 01 Nov 2023 16:56:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63c4a2c988c14d91bd1bb24d26d73d206d9ca3a20b02760ebf137a1fbd73d42`  
		Last Modified: Sat, 04 Nov 2023 00:15:51 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48418e23975922d413d904980fa6f97cacdcd980409557f2d959ecb456922426`  
		Last Modified: Sat, 04 Nov 2023 00:15:51 GMT  
		Size: 347.2 KB (347164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6ebee071287832fcba5251da1c84bf8265763aefcc8b5edfbe0bd4f9754370`  
		Last Modified: Sat, 04 Nov 2023 00:15:53 GMT  
		Size: 14.2 MB (14168086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457e891302ca82df971b55e117ff3f4b90396a1ccdf80a98c1a873938daa9078`  
		Last Modified: Sat, 04 Nov 2023 00:15:51 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa69c17c153f76d4cc7af2b0306c9396a62a03fbd8e21b82a02a2bbc1f4bfe9`  
		Last Modified: Sat, 04 Nov 2023 00:15:51 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:c32ca261981bea69ff2a9d2ec1c5fea5b23610506c29a818275db3269fa96d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17132612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84556a029b21119037c2f8a5df0812fd7bdc7fc79b534f68a8316e44cb89a050`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_VERSION=7.2.3
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.3.tar.gz
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_SHA=3e2b196d6eb4ddb9e743088bfc2915ccbb42d40f5a8a3edd8cb69c716ec34be7
# Wed, 01 Nov 2023 16:56:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
VOLUME [/data]
# Wed, 01 Nov 2023 16:56:23 GMT
WORKDIR /data
# Wed, 01 Nov 2023 16:56:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 01 Nov 2023 16:56:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8bcc30219a3b5ad7547cb998dbc925d87391c679fec1abae88483d4839fa51`  
		Last Modified: Tue, 03 Oct 2023 23:23:43 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1e96038724920ff29465fba0c7aca16d709e1f1d94b903204ed8b6af9e8387`  
		Last Modified: Tue, 03 Oct 2023 23:23:43 GMT  
		Size: 347.0 KB (346994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e77fcdc624740cb8fbc9318efec08025976fa8ba59f2c0004fb6ed1138a599`  
		Last Modified: Sat, 04 Nov 2023 00:58:20 GMT  
		Size: 13.9 MB (13883761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8513047b885df6344a1af8cd8e4989dba9ada42824812d8cfcc832dfee3a39`  
		Last Modified: Sat, 04 Nov 2023 00:58:19 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db04884293261c32ab745b7654e0f4ac08b0125b590bd2422cd85e457f1c1f6d`  
		Last Modified: Sat, 04 Nov 2023 00:58:19 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:01a13277c400b0c60119d4c0738ae1176954e370860873e46095598c9eedab88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.3 KB (719306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a640255e85017dfee867b7b6bcd678b86cdd774142bb62f3e5799ec367609727`

```dockerfile
```

-	Layers:
	-	`sha256:86f4c1f3135f481f11fdea65ef30269e3ca817a81e0cb9274d788a35ca898f5d`  
		Last Modified: Sat, 04 Nov 2023 00:58:19 GMT  
		Size: 692.9 KB (692915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:421d04d0292947c746bf2f0b1a7cfe9c3bf452ff49374b6ca9f62f2393ae1eb9`  
		Last Modified: Sat, 04 Nov 2023 00:58:19 GMT  
		Size: 26.4 KB (26391 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:d12163b11c4beaf35614be1b1a9682da599a13d173cf0ab5f5ace330b9a30e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18084744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b697ced7a6e4c9aa0b81e4fa0d88bb69324dbb6be9834181f074518d94fd887`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_VERSION=7.2.3
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.3.tar.gz
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_SHA=3e2b196d6eb4ddb9e743088bfc2915ccbb42d40f5a8a3edd8cb69c716ec34be7
# Wed, 01 Nov 2023 16:56:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
VOLUME [/data]
# Wed, 01 Nov 2023 16:56:23 GMT
WORKDIR /data
# Wed, 01 Nov 2023 16:56:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 01 Nov 2023 16:56:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0feb8fddc533ebe8fa3e28ab60443a2b6a5a7e46ff3560b1e79f4ff945a70f`  
		Last Modified: Tue, 03 Oct 2023 23:02:00 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a743b36a722987becef2b73971d75377bee67a2a6577cbdfddc1da3634eb4a73`  
		Last Modified: Tue, 03 Oct 2023 23:02:01 GMT  
		Size: 347.6 KB (347581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543ffaa390ab69d3a7ff460ce86e4ba9fe69237b94508a69dc09590c692731f2`  
		Last Modified: Sat, 04 Nov 2023 01:27:12 GMT  
		Size: 14.4 MB (14403384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51804ef2b3e7243c80e60c9d5231d7e514b0cb28a670ba8b07fe35b1f75afc46`  
		Last Modified: Sat, 04 Nov 2023 01:27:12 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d155bcddaab4fd7ce2f26474314f8b6b0bcc8b10ebed5bbb6cffb55070c4861`  
		Last Modified: Sat, 04 Nov 2023 01:27:12 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:0fbdea79cdc0fcdd372544f8a9712385f2c4f00aa29dbe4654bac106dc77fff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 KB (716658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44a4b7eb19d72e0645c8613b7f739ed87b709fa1d5c03e9f63dc8e6422b8b54`

```dockerfile
```

-	Layers:
	-	`sha256:a395ff52bfa81315cc2290a6e7518a6be3559eef76b37f217193e6ad90162d5c`  
		Last Modified: Sat, 04 Nov 2023 01:27:12 GMT  
		Size: 690.4 KB (690390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1879b625b29a3be34166f4d38cc82daeef1622b3f30a63bfd9a388c82dc2799`  
		Last Modified: Sat, 04 Nov 2023 01:27:12 GMT  
		Size: 26.3 KB (26268 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:aa9dc6761b6f8f71796b2ce3700d48472d2ab8a5494a2ff22dc7a0d90d77144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17371869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3f7fd026f58a172e1cdb492b5e35f3779b8c93f93c88dff88083dc3503fe53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:38:19 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Thu, 28 Sep 2023 20:38:20 GMT
CMD ["/bin/sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_VERSION=7.2.3
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.3.tar.gz
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_SHA=3e2b196d6eb4ddb9e743088bfc2915ccbb42d40f5a8a3edd8cb69c716ec34be7
# Wed, 01 Nov 2023 16:56:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
VOLUME [/data]
# Wed, 01 Nov 2023 16:56:23 GMT
WORKDIR /data
# Wed, 01 Nov 2023 16:56:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 01 Nov 2023 16:56:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ba638cd9c74c2570d6e68edb4d19831d4c65064424f614e651fe60d12850c5`  
		Last Modified: Sat, 04 Nov 2023 00:03:19 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdec2761f7c9b3d7ab9c0de9990ee8cc6794a57c8e2ca5ee47143c57c32a5ca`  
		Last Modified: Sat, 04 Nov 2023 00:03:19 GMT  
		Size: 347.4 KB (347384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d58bc8b6ecb0e5cf9dfa04905f8813d211ebdb5b4905f44a43f989e87c27e2`  
		Last Modified: Sat, 04 Nov 2023 00:03:20 GMT  
		Size: 13.8 MB (13786777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b2d08907cb2d39691f9ade7907ac921a9e1c53e836947684f1eb59d2d7dc7`  
		Last Modified: Sat, 04 Nov 2023 00:03:19 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0806d930b0b74b0f7a58593c281d48cb8d3307d50bb094ed21c06b1bd2720fb`  
		Last Modified: Sat, 04 Nov 2023 00:03:20 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:e9054dfb62b0f41f88a18627bdbf3396fe1653adfec9990fab8f26bfed3da465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f149987d135976df961ee2f0c1d47ecd9af2782025f4343d8a21b47897fa32`

```dockerfile
```

-	Layers:
	-	`sha256:612873743f62d6da907754c1af029c9fe3043a84304761780847b5b894fe1023`  
		Last Modified: Sat, 04 Nov 2023 00:03:18 GMT  
		Size: 26.1 KB (26146 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:6ab6870316d564bc078e854fbe8b2e3d3708007f45a5164bb767dc079d544a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18786094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2fea727c018673d960e18d9342b822400776ee16aa2af96d36c75d97591a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_VERSION=7.2.3
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.3.tar.gz
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_SHA=3e2b196d6eb4ddb9e743088bfc2915ccbb42d40f5a8a3edd8cb69c716ec34be7
# Wed, 01 Nov 2023 16:56:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
VOLUME [/data]
# Wed, 01 Nov 2023 16:56:23 GMT
WORKDIR /data
# Wed, 01 Nov 2023 16:56:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 01 Nov 2023 16:56:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e963944e7d7c85e7e5202f0596efabc5d145dfc37f6e0a9b481b7e185470e576`  
		Last Modified: Tue, 03 Oct 2023 23:04:16 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c07f1f59e5142c61f551a02105a3fe01c28e7ae009ba3c9ef69dc54d2c90a8`  
		Last Modified: Tue, 03 Oct 2023 23:04:16 GMT  
		Size: 347.6 KB (347649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b89e6806154e077eed9c39ce876184f8c7e38f91239c845cb4a44de5e8b0250`  
		Last Modified: Sat, 04 Nov 2023 00:33:15 GMT  
		Size: 15.1 MB (15089986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9203618aed55ff47bfdbc24dc7fed4e697ed8e392dfee180372b86de64cde40`  
		Last Modified: Sat, 04 Nov 2023 00:33:14 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfaffd107fd93f4aea5a436a8c25a447b52f6acd080f845f06c735c34bc6010`  
		Last Modified: Sat, 04 Nov 2023 00:33:14 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:fe5053687dfe67f8cd281e0af022aa7a8b794b9bb2ab7e05df5fb89724cdc10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.1 KB (715111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d957d07249a7deecae2f1d98995a2264aa8e7397bddf8a76a361b930cc87e94`

```dockerfile
```

-	Layers:
	-	`sha256:5730bf353afdd18f9a62e6067ba1cf56a9d3df67d9b59ccb53840f75b4670d0f`  
		Last Modified: Sat, 04 Nov 2023 00:33:14 GMT  
		Size: 688.8 KB (688793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56a816069fafcda5222e9d81676b73e4ac05f1a3d7b4a5088497bf8e050e4962`  
		Last Modified: Sat, 04 Nov 2023 00:33:14 GMT  
		Size: 26.3 KB (26318 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:29fa419ba018340c61da212e2fb79fcd295be66889d516e2ce55b6fc0754990b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18043540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1634b031043878017eb82d8de00541093f84139869e15a513b8d9557bbf8a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_VERSION=7.2.3
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.3.tar.gz
# Wed, 01 Nov 2023 16:56:23 GMT
ENV REDIS_DOWNLOAD_SHA=3e2b196d6eb4ddb9e743088bfc2915ccbb42d40f5a8a3edd8cb69c716ec34be7
# Wed, 01 Nov 2023 16:56:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
VOLUME [/data]
# Wed, 01 Nov 2023 16:56:23 GMT
WORKDIR /data
# Wed, 01 Nov 2023 16:56:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 Nov 2023 16:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Nov 2023 16:56:23 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 01 Nov 2023 16:56:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8fb319e3e2b6d090a150207805753dae05abe1df53b9dae9b211d46986bb8e`  
		Last Modified: Tue, 03 Oct 2023 23:15:31 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8fdacac4cf0c35819b1f0be78d8bed53f4dfdce11d17b3918d554a29299129`  
		Last Modified: Tue, 03 Oct 2023 23:15:31 GMT  
		Size: 347.4 KB (347360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936ebe1010f2aa45430e56a5676ba14e0e4cf647a9e8aa006b74578a3c4a3b5c`  
		Last Modified: Sat, 04 Nov 2023 00:34:58 GMT  
		Size: 14.5 MB (14479128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b06512c5673bd618a915a4e13f3d9a567bd17f21d7d71c5d78e05b70a4882c6`  
		Last Modified: Sat, 04 Nov 2023 00:34:57 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f88314cc71da96f8ebfcd7a2fa9e178468e6016390eb4a312f7fa8ebfb83a3`  
		Last Modified: Sat, 04 Nov 2023 00:34:57 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:ba886e4c79382a42623531879d9f7db33698377c3087caf39e7b5c5de71a51a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.0 KB (714982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36564870e89e34fb90c1d98900c311efd009756487e14d9694ea2542211d18cc`

```dockerfile
```

-	Layers:
	-	`sha256:180f82fe8892edff4d7147bd8101d5b629e0b602b89adb328381d56db413a94f`  
		Last Modified: Sat, 04 Nov 2023 00:34:57 GMT  
		Size: 688.7 KB (688735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd770f260c01058912ac66d23ab58a0921c2671fe025ffd30111ce0b88484ef5`  
		Last Modified: Sat, 04 Nov 2023 00:34:57 GMT  
		Size: 26.2 KB (26247 bytes)  
		MIME: application/vnd.in-toto+json
