## `redis:6-alpine`

```console
$ docker pull redis@sha256:eae76512623bdaa06bcf3b7213cdb055ad2c5ebd08636aba0186948276aee724
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

### `redis:6-alpine` - linux; amd64

```console
$ docker pull redis@sha256:b94bf93e379f598b0517c853b2007a214b7579aae59f17c7e45c93504a6f1c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529fcf955ad4a13d88796dfa488ed12f652f7e12c37eaac62f752a8cc47f5d5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 10 Jul 2023 15:03:13 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["/bin/sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_VERSION=6.2.13
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Mon, 10 Jul 2023 15:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
VOLUME [/data]
# Mon, 10 Jul 2023 15:03:13 GMT
WORKDIR /data
# Mon, 10 Jul 2023 15:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef610ca56b27912b3247efc4e94db9be9c100d11381ee53a5a6897952486055`  
		Last Modified: Tue, 17 Oct 2023 19:01:43 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97db018d5f756cd58ec62c9f09797a8d68d9637becbc535ea0be91a16ac80b0`  
		Last Modified: Tue, 17 Oct 2023 19:01:43 GMT  
		Size: 347.4 KB (347371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f153e715778f59453643066ad54100584132ae7fa28c7140bbd56bc307dc7693`  
		Last Modified: Tue, 17 Oct 2023 19:01:44 GMT  
		Size: 7.9 MB (7926788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0180be8a88a90106485c9cc18af79e0808301b2e0938a91801e16f38c369fa8`  
		Last Modified: Tue, 17 Oct 2023 19:01:43 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129f5a5ab4effa9c7694225794aeecde3551fb93489f7f4f6220eebe817dcb37`  
		Last Modified: Tue, 17 Oct 2023 19:01:44 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:8b427e9dcf33badc9a564b446e6ad54e4858babdc3d8c0e271c51253d8de5a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.5 KB (751500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fa82020936340e3d1aab862b97b2ab620e31d14b18ee4c46c8d5438e62286d`

```dockerfile
```

-	Layers:
	-	`sha256:5220d0de759c2b860535b660a4cecada2b002797999cdf0ba97f73b3513b7e6e`  
		Last Modified: Tue, 17 Oct 2023 19:01:43 GMT  
		Size: 725.8 KB (725838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad2deb48fe872cb533683b3a3a607287769370247f7bf98699a7612482806c4`  
		Last Modified: Tue, 17 Oct 2023 19:01:43 GMT  
		Size: 25.7 KB (25662 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:40f2ce1732661bc625f73afae8e4e3d191fd6d5542a8c2f283038899bd3637b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11070277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff453987c95273a93609532c0896ba5d471999c117e51d36cabc54db80e601bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 10 Jul 2023 15:03:13 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["/bin/sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_VERSION=6.2.13
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Mon, 10 Jul 2023 15:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
VOLUME [/data]
# Mon, 10 Jul 2023 15:03:13 GMT
WORKDIR /data
# Mon, 10 Jul 2023 15:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a61b7be475a718c982548ef463e0c9e4a89c8e4295022c7ff8dd1ca8f9b9bf`  
		Last Modified: Tue, 03 Oct 2023 22:59:50 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c175be1a443b134a9e8b9971f24266cb06f3e831d2d20258a597465cab769c5d`  
		Last Modified: Tue, 03 Oct 2023 22:59:50 GMT  
		Size: 347.1 KB (347147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ca4099fdf5bdf31d1c52172aa80c273648e5b2fafb3b1e143b842a29c39055`  
		Last Modified: Tue, 03 Oct 2023 23:02:04 GMT  
		Size: 7.6 MB (7575890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a895cdfb88b8e0c2331ba450e0722863e2b1be2067cb097d44bebbd70da5a3d`  
		Last Modified: Tue, 03 Oct 2023 23:02:02 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025b02f31a238f347da2a8d82d1de5600e9764262860df7e1df4dfa146716ab`  
		Last Modified: Tue, 03 Oct 2023 23:02:02 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:26b3f746523a24c6f67c984f9a024b2bbc643e4e3c4c67680c747ccde092efa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10710716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3f0670f7a68b1bf5b667732b376f2e8f0b5cff82e2d597e73c89190d2f3fd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 10 Jul 2023 15:03:13 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["/bin/sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_VERSION=6.2.13
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Mon, 10 Jul 2023 15:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
VOLUME [/data]
# Mon, 10 Jul 2023 15:03:13 GMT
WORKDIR /data
# Mon, 10 Jul 2023 15:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 10 Jul 2023 15:03:13 GMT
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
	-	`sha256:a26db50a590f30eba00a3f38b8aa189cfb57ddfb1cce931e3470f06aa1225947`  
		Last Modified: Tue, 03 Oct 2023 23:27:58 GMT  
		Size: 7.5 MB (7461869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcc5ba87a65e106b801edf8584a956744348456962cb55a874e32687df03659`  
		Last Modified: Tue, 03 Oct 2023 23:27:56 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d56d01bd817ea16025fbaab5aac7cf784e761c9206b735de2b435bc8504845`  
		Last Modified: Tue, 03 Oct 2023 23:27:56 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:e869a3161fe2f2a21f520bba56e111b87c724428702366be4372f9c1d5a44ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.1 KB (753072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad3f5f9db6a5a2598a6b504d5ac78444edc484b5902b91eedbaec1a1271d968`

```dockerfile
```

-	Layers:
	-	`sha256:fefecd2868bc1b1caaddae745204e965c53297fd888753310c3436f1ccbf6dca`  
		Last Modified: Tue, 17 Oct 2023 19:11:36 GMT  
		Size: 727.5 KB (727453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5777dbbd2b39afda3a8d81b8361adac8fb1be5047c6ca080c7681ef6ebb09cfb`  
		Last Modified: Tue, 17 Oct 2023 19:11:36 GMT  
		Size: 25.6 KB (25619 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:4f7d75793a5a33d710b34f02cc17af6ec68168824966d3dd1b1c68f64dc35162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11278978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e9cd81b1a0ddb38c8f2cd2bd307e8edd58ade8daff3a801efacaf3df91c0db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 10 Jul 2023 15:03:13 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["/bin/sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_VERSION=6.2.13
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Mon, 10 Jul 2023 15:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
VOLUME [/data]
# Mon, 10 Jul 2023 15:03:13 GMT
WORKDIR /data
# Mon, 10 Jul 2023 15:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 10 Jul 2023 15:03:13 GMT
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
	-	`sha256:18ff94ebdc1a2bb2fcbda57f4cd15a4159a074449e0e4a434ddf49c6776625ae`  
		Last Modified: Tue, 03 Oct 2023 23:05:46 GMT  
		Size: 7.6 MB (7597619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d73e6c3e1e09af4ce8645483d58c00bfde226e5824b0d061d4491a6fbd982e`  
		Last Modified: Tue, 03 Oct 2023 23:05:45 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c3610ca27caf5b9793fde34e6b4e312cb0028993393b3f9fd9dd6fdaaec7f`  
		Last Modified: Tue, 03 Oct 2023 23:05:45 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:d77081dc65687842dc743f8b4fb19871fe7496e04f6a80fb89c9975b14bf1f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **750.5 KB (750455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07c6401a2e2ee45392f878439eb69ad751a4809962a68c14616d5d4c5e3763`

```dockerfile
```

-	Layers:
	-	`sha256:6726ca0ae163d228d43de05536df213c4a6621ca761cd6fb829413c46100456a`  
		Last Modified: Tue, 17 Oct 2023 19:07:07 GMT  
		Size: 724.9 KB (724945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a113930495845c0a055e892e301e662c5db7e3db2395d08a72f66c8437113a`  
		Last Modified: Tue, 17 Oct 2023 19:07:06 GMT  
		Size: 25.5 KB (25510 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; 386

```console
$ docker pull redis@sha256:9a902b9f91c0f000733d021305c6c2211b277370e5ef5b76f884e495ce13750d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11249819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ff8cd7b8e3cc692cf85e383d8f20a00f146ae2c91deefa954dd09ebb300f22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 10 Jul 2023 15:03:13 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["/bin/sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_VERSION=6.2.13
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Mon, 10 Jul 2023 15:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
VOLUME [/data]
# Mon, 10 Jul 2023 15:03:13 GMT
WORKDIR /data
# Mon, 10 Jul 2023 15:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e574fadde04462851839e1801a70c5964eecf52f23dfb3cea251602d689280f2`  
		Last Modified: Tue, 17 Oct 2023 19:01:20 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d506ccf10c5ca57c3b1116244f11819f5a22025d5e8b182b03d3231480e5cb`  
		Last Modified: Tue, 17 Oct 2023 19:01:20 GMT  
		Size: 347.4 KB (347371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5df6495d5058731f829565111a5ef65e9d835240e0802e9dab4f2b5933a11fc`  
		Last Modified: Tue, 17 Oct 2023 19:01:21 GMT  
		Size: 7.7 MB (7664741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46cdab9748c12e8d08a065b0de4f1261655b8738744161b62a2e0b0f92fc59`  
		Last Modified: Tue, 17 Oct 2023 19:01:20 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c55ac06809ada6e5ee9c826a678e34044066d4eb80a368b357c70906e3bbcf`  
		Last Modified: Tue, 17 Oct 2023 19:01:21 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:3b5d12ff89b1baacd40d0e673527d2b7e782ac14de1669ebc75d21b5b5d1f8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee66880d22a4b99ccc9458cc0a72e4c2a2d250027d7e644f04178a92ecbd887`

```dockerfile
```

-	Layers:
	-	`sha256:7ba514d64e98512a12cdd950077a33c24c7dc39533fcef130dacce99a7ecf48f`  
		Last Modified: Tue, 17 Oct 2023 19:01:20 GMT  
		Size: 25.4 KB (25399 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:eb8f6626e6e593ed417d1a960171b5980432c0ada0542c2cc841a98d312261d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11835412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cf026ba227438436181848267163cb253a1296d67f30edb086f118f92a0699`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 10 Jul 2023 15:03:13 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["/bin/sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_VERSION=6.2.13
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Mon, 10 Jul 2023 15:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
VOLUME [/data]
# Mon, 10 Jul 2023 15:03:13 GMT
WORKDIR /data
# Mon, 10 Jul 2023 15:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 10 Jul 2023 15:03:13 GMT
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
	-	`sha256:3387352c8d066de6277eab379fc66098870e86e3ed6e3e8023d2b3ad0b77ee9b`  
		Last Modified: Tue, 03 Oct 2023 23:12:14 GMT  
		Size: 8.1 MB (8139306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab16c9127d3ba88f526cdaffe3d80d81d75d5acad06e6646dd958a88969b2383`  
		Last Modified: Tue, 03 Oct 2023 23:12:13 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98252c7ecf7bdbd8aa9748847ebbb954115d2647639bc909ae4f0d8a9860357`  
		Last Modified: Tue, 03 Oct 2023 23:12:13 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:1d6b659937b75f2f3730c860c4a21bbc5353700708196820f1916ffb1b8f07f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **748.6 KB (748601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf592a6e2245c990b94384d42744bb6471ade4c702fbcf4a8070d1c1d1f8f5f`

```dockerfile
```

-	Layers:
	-	`sha256:7b2bf6cbe95d38d9cec9ef05f8393293e4ce2862dd7757f63a611c3d441dd7c5`  
		Last Modified: Tue, 17 Oct 2023 19:08:41 GMT  
		Size: 723.1 KB (723054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4475823c4339954510ac73a3f42c4cb1ea4ed566268a1a8be8c50ae23c4180e`  
		Last Modified: Tue, 17 Oct 2023 19:08:40 GMT  
		Size: 25.5 KB (25547 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; s390x

```console
$ docker pull redis@sha256:82dd8936c1a2c57ece29f6357bfb0dde1a134c3cd183081893fc2d3f72d52bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11390485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fc3fa4031cd5e6dae99d62970dfbaed0733a41ccef705ed6f3e74a5aceb854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 10 Jul 2023 15:03:13 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Mon, 10 Jul 2023 15:03:13 GMT
CMD ["/bin/sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_VERSION=6.2.13
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Mon, 10 Jul 2023 15:03:13 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Mon, 10 Jul 2023 15:03:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
VOLUME [/data]
# Mon, 10 Jul 2023 15:03:13 GMT
WORKDIR /data
# Mon, 10 Jul 2023 15:03:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jul 2023 15:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jul 2023 15:03:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 10 Jul 2023 15:03:13 GMT
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
	-	`sha256:0ffff3be7cc09fee7a531d2a24b51da505a0c05e497716d2dbebd3b61caf196e`  
		Last Modified: Tue, 03 Oct 2023 23:37:37 GMT  
		Size: 7.8 MB (7826073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f251b5c040797113983e824fcbbd1c658da1b7401998ea9c89358def0c477fc6`  
		Last Modified: Tue, 03 Oct 2023 23:37:37 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652a5313f8bcde5a2a03742ea1fe899d1c3159ded4b63aad180e43465786fbf7`  
		Last Modified: Tue, 03 Oct 2023 23:37:37 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:c3ec37a0f07e66bad258f4b7cf2980786817c8788c6ff488af57b2f9a8e05df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **748.5 KB (748492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a99acc788d5a315ee7ca85fdbcb7f6688c37e610e28da981b27ac4181a91aff`

```dockerfile
```

-	Layers:
	-	`sha256:65357d02ab39c3e5317fcc9fadadf586381bdc55a61e5b5ad1d35c67c8232530`  
		Last Modified: Tue, 17 Oct 2023 19:08:35 GMT  
		Size: 723.0 KB (722996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4319127d4d22c6d5ed7bcb5c455faffa2283a260367cbfacd13f4edbb9ee24`  
		Last Modified: Tue, 17 Oct 2023 19:08:35 GMT  
		Size: 25.5 KB (25496 bytes)  
		MIME: application/vnd.in-toto+json
