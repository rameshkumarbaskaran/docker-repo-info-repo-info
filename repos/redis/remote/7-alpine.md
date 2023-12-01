## `redis:7-alpine`

```console
$ docker pull redis@sha256:84e41163d6ad18e0653b0e6e58484d93eb3f0dd387c4466b9da84adc31cb853f
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

### `redis:7-alpine` - linux; amd64

```console
$ docker pull redis@sha256:9e3f3a58c85904fe2d40088b5b69dfe688ba3eff91320f2849df3eeea5d2bf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15624494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6420819df1b0de1008141a23b4a6fa4c658ff699e2f10db129b7891b7256661`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 10 Nov 2023 15:23:15 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Fri, 10 Nov 2023 15:23:15 GMT
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
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ee276465ceaeddd42b045aaa18ed436174e65b326ca2e24e1f32051740a3ae`  
		Last Modified: Fri, 01 Dec 2023 00:12:15 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba2c8f9b916fe6173a82e0a4aa979410387f773c7a166e80c37f070d30ce322`  
		Last Modified: Fri, 01 Dec 2023 00:12:15 GMT  
		Size: 347.3 KB (347309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86024d2069a54ad7df24ef5c1c9c31df78ceff57605358f363f5da94dad684f7`  
		Last Modified: Fri, 01 Dec 2023 00:12:16 GMT  
		Size: 11.9 MB (11872823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc50070e1a927919dc3852040dc3a6c20b1804e02cc4feba592ab5f86f1f9205`  
		Last Modified: Fri, 01 Dec 2023 00:12:15 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1605eb5694a43274f94c9f23da092574c7e3ebe12b568a79f1a610e69d6587`  
		Last Modified: Fri, 01 Dec 2023 00:12:16 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:c05a452c4af9eb319648dbdd347ede6e897079ae4b149641e75ce9e7ef1be024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.1 KB (718065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cea50775c389bd3b07958bb5eba5d745c57afb34233b75b3349063b27e985cc`

```dockerfile
```

-	Layers:
	-	`sha256:0072bf82dee999dde07f60c1bc273806a9910295c3d57dbc24ac0ac5854bee64`  
		Last Modified: Fri, 01 Dec 2023 00:12:15 GMT  
		Size: 690.5 KB (690530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4dc7d2b6e1c7aabb54d2c8abcd5f33508cda341ad57789beaff59d47cf867d`  
		Last Modified: Fri, 01 Dec 2023 00:12:15 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:51a49eaa042ef1661290eede107a8b08cfc49e97d411dbd0a1ca5c25047e2244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17662977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8b69849dcebedc73f43e4eace58f5027b2d8f34899bb0a52032dc6d4048b1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
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
	-	`sha256:3ff1be6d21a4e1cfbe3c01dd714be73f4e369eb0154a6ae6d9340c51e180c113`  
		Last Modified: Thu, 16 Nov 2023 01:23:37 GMT  
		Size: 14.2 MB (14168578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38ee51022a80f8a4d396c4c132e6cec009d1e6305acee8dd9c86a33dfb6f088`  
		Last Modified: Thu, 16 Nov 2023 01:23:34 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f43529154f4a50fe7940d85032673aeaf5a8dbd09a08678abc0fddb6128ab9`  
		Last Modified: Thu, 16 Nov 2023 01:23:34 GMT  
		Size: 567.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:b0b8f54fcdc7c6e686189b7004f17cb04f7924496a0c1b3ba1dc54b5946ffb62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15139650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0209ff74ef8a459089300d73037501e292b8756a6ba5a6110b5b6fd694a8f36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 10 Nov 2023 15:23:15 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Fri, 10 Nov 2023 15:23:15 GMT
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
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1506ef5fd24d7f718f4fe36a0f415b1813ab739f8b6f4980aef5dd6b52b2baa1`  
		Last Modified: Fri, 01 Dec 2023 11:53:20 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62980244a675df70d66eb7e32695d7de4f436510ed34e29439cdd35eef6999e5`  
		Last Modified: Fri, 01 Dec 2023 11:53:20 GMT  
		Size: 347.0 KB (346973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3245056ee1029b3b70d4a1f27e6cb76fe146f749320e64c22d0bc4d33c5602`  
		Last Modified: Fri, 01 Dec 2023 11:53:21 GMT  
		Size: 11.9 MB (11889728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ecc406e4a689c89463f4a9224a7820979aaecb243cd361fec508a7653f611`  
		Last Modified: Fri, 01 Dec 2023 11:53:20 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3495f10b62b30a6429ee06f159defbb1cc18d18bd727c618200ea14c5d4b77a6`  
		Last Modified: Fri, 01 Dec 2023 11:53:21 GMT  
		Size: 567.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:bf706ae317812c49cb69b41160466eb39860323f771077fde345c7e930095634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.6 KB (720584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03f09c520ef78e3fe7d60193d0013bfcb1188a816af897c491009338831c727`

```dockerfile
```

-	Layers:
	-	`sha256:89c587f254613a7f67d3c509199e8c9a6f0d7b79ad757e4b8b4b310d0e3f013d`  
		Last Modified: Fri, 01 Dec 2023 11:53:21 GMT  
		Size: 693.1 KB (693074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6cdc4d1e363b3436290090146d5cbe2b2bc52700867d332e976557bd6777229`  
		Last Modified: Fri, 01 Dec 2023 11:53:20 GMT  
		Size: 27.5 KB (27510 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:43076a37580453c7d2516cff8e4aa6b5a8af2c86366ff8b8b4bde0b0b1fb0c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9825906c4729a1edf445de2a66ab546115b54f915a009b396c96bd412d43735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
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
	-	`sha256:e921a448359a4fec1c9fc2b03da1676cc4a0cbce73a7ff503faafc2128f3f070`  
		Last Modified: Thu, 16 Nov 2023 01:36:33 GMT  
		Size: 14.4 MB (14403801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead72011169f10ebef949b2a6c940c6190ebbed1146fb53b8edc2dff870d3d21`  
		Last Modified: Thu, 16 Nov 2023 01:36:32 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6335bc74acc3ee6c090362f9f80d236e7955e347e8198a46c0860d058478df7`  
		Last Modified: Thu, 16 Nov 2023 01:36:32 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:4ff411fbb9a1ef2e1b78399b3629d44b22c902c2caf9cb49a58634b6c1eb9fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.8 KB (718803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ca52cf96a1847941fe639363ffe04d0a90df49e222a3e56cc60e6e14b53454`

```dockerfile
```

-	Layers:
	-	`sha256:de880ad0e056e005a63ee3ffb9425fe45fcfb58f2075287a089bd663eaad5030`  
		Last Modified: Thu, 16 Nov 2023 01:36:33 GMT  
		Size: 691.4 KB (691416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0170c07b267b2d700f2d071909e7c71ce5b7ef6ae51604d7304f424d468ca514`  
		Last Modified: Thu, 16 Nov 2023 01:36:32 GMT  
		Size: 27.4 KB (27387 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; 386

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

### `redis:7-alpine` - unknown; unknown

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

### `redis:7-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:03156658d164dd3c5522819c9ed5738da641947a1a2cbb6ce9bfd3a23fc33105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16444761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c9a03b1afda99f72adbbd0977901ff287a12636583cdc3ce1af41e72241667`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 10 Nov 2023 15:23:15 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Fri, 10 Nov 2023 15:23:15 GMT
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
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d838ff435f29e2ab4eac4b792b25be0ed7646e56a1e0123ef076df6a24d5f7`  
		Last Modified: Fri, 01 Dec 2023 13:00:58 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5c9eca873bc348a1c5e4a07292eb197e0d824e0b6f759acf6e637aaa4246e2`  
		Last Modified: Fri, 01 Dec 2023 13:00:58 GMT  
		Size: 347.7 KB (347655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116c7351cccd52cb84e8bf8610ae9355c056834ea9e85f4d5655d50b84660fad`  
		Last Modified: Fri, 01 Dec 2023 13:00:59 GMT  
		Size: 12.7 MB (12746835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03ef4ddb3be99c5dea2a9f3b45303dc9a61918f8825096c27ea94f5590e9591`  
		Last Modified: Fri, 01 Dec 2023 13:00:58 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398db60f320004b73a75adf42b944acb5f19156f0d4eb247b5fd353a333b386d`  
		Last Modified: Fri, 01 Dec 2023 13:00:59 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:89c1f07ff6debf9997d252dd52809bf257f6e050bf1f7269eebe08d8a1397fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.4 KB (716389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f508d3ef66e266b8f916812e95b5cd6eef66004a0c5ea885630e29b04b978e`

```dockerfile
```

-	Layers:
	-	`sha256:b815684fdc23cc967713b39fb391239e8f55b2f75f6a0056809085523d014895`  
		Last Modified: Fri, 01 Dec 2023 13:00:58 GMT  
		Size: 689.0 KB (688952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffd2637a1a5d46934f8ee9536ed6522e22b014527d40accb3f53e9afd202a1b1`  
		Last Modified: Fri, 01 Dec 2023 13:00:58 GMT  
		Size: 27.4 KB (27437 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; s390x

```console
$ docker pull redis@sha256:0f8e1c3ae127b833489b0c01e5fea22c716536fdee149a3974c0b9e53f226225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15816259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc40689fe37e70c2247bac6cd1fdf13aa142fdf217668e12514fd9121829da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 10 Nov 2023 15:23:15 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Fri, 10 Nov 2023 15:23:15 GMT
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
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e6dd364dbbcb95d95bf4b0b2cec1273c6f92a8b8fb677cf42d41a68c140b14`  
		Last Modified: Fri, 01 Dec 2023 12:23:54 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e329ccf1820b22a93f390432f82d6899038db625bc0c3195393a0aa8ccbed6`  
		Last Modified: Fri, 01 Dec 2023 12:23:55 GMT  
		Size: 347.4 KB (347368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b47cd424336dd0569afa234cfb5f1f7682633d69c2580b60d3c5a33bcd0f62`  
		Last Modified: Fri, 01 Dec 2023 12:23:54 GMT  
		Size: 12.2 MB (12249487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e089b766be8861481ccac73c532dfff7495349cd51cb4083d15d2deb586615`  
		Last Modified: Fri, 01 Dec 2023 12:23:54 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1b0a1c5798f9a7f0d751d5d29f7fd9e4b15c44c5b16b27fa0b839dcb1c89e8`  
		Last Modified: Fri, 01 Dec 2023 12:23:55 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:599ba6eaab908bafe599f70df049ee1bd8e5bfcdd3d82aed3360e2ff3c7892e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.3 KB (716258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3eabfea5934b067b776d20098495830df5e17f7fb3bf915c22fbeb2c0226f2`

```dockerfile
```

-	Layers:
	-	`sha256:49a4d628cc1c8351dad14809566368d1eff5a22c5745c98f51be8e3d45bee371`  
		Last Modified: Fri, 01 Dec 2023 12:23:54 GMT  
		Size: 688.9 KB (688894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:059771f5402a86fd0ee819a8d1d72b2f8f46b8f4886c8c99211521682c7f07de`  
		Last Modified: Fri, 01 Dec 2023 12:23:54 GMT  
		Size: 27.4 KB (27364 bytes)  
		MIME: application/vnd.in-toto+json
