## `redis:bookworm`

```console
$ docker pull redis@sha256:e207d297b9722053d0369be627633433fa6e1d1447a42539964ff5849327545a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `redis:bookworm` - linux; amd64

```console
$ docker pull redis@sha256:178215249742b63308db1a5373a7c627714c582362f3dcd24b2eec849dc16e67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48125584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e69fcb59ff4a25f87cf68cf2558df9c56df3c3c8ef709677dc602a458fe9b2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 21:53:38 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 14 Jun 2023 21:53:38 GMT
ENV GOSU_VERSION=1.16
# Wed, 14 Jun 2023 21:53:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jun 2023 21:56:11 GMT
ENV REDIS_VERSION=7.0.11
# Wed, 14 Jun 2023 21:56:11 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.11.tar.gz
# Wed, 14 Jun 2023 21:56:11 GMT
ENV REDIS_DOWNLOAD_SHA=ce250d1fba042c613de38a15d40889b78f7cb6d5461a27e35017ba39b07221e3
# Wed, 14 Jun 2023 21:57:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 14 Jun 2023 21:57:04 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 14 Jun 2023 21:57:04 GMT
VOLUME [/data]
# Wed, 14 Jun 2023 21:57:04 GMT
WORKDIR /data
# Wed, 14 Jun 2023 21:57:04 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:57:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:57:04 GMT
EXPOSE 6379
# Wed, 14 Jun 2023 21:57:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bc4b7ad0f02fe99bf6836ed4f7cb4509d9c7d94627ace9f43133fdbeaf764e`  
		Last Modified: Wed, 14 Jun 2023 22:01:30 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33d2f01ead9ae4e9f5bf12af82045ef150407cc8098dd0decaaee54ac36f4f0`  
		Last Modified: Wed, 14 Jun 2023 22:01:30 GMT  
		Size: 1.4 MB (1436811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b33095e71ca50a19c4e55bf6e70638c6391dece2b7281720c2b284c61218a0`  
		Last Modified: Wed, 14 Jun 2023 22:02:01 GMT  
		Size: 17.6 MB (17562202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c2b649b97ccdfb269abba0191215f9d5a3c6ee4aa72210c74a25220c9143d1`  
		Last Modified: Wed, 14 Jun 2023 22:01:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5bf7f0acd78ea73ec7fd047448cac874569cf69b57568668553c3f7bf35f83`  
		Last Modified: Wed, 14 Jun 2023 22:01:58 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:0f0d8346b066dcb75f759ef067b0b6bd0ac62afa3d49039f515ea095e1be5e07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44266222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53555cf86c6cf034518db9cec88befc7a3cc8e0dbb0a677af7f6d6a68e258626`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 12 Jun 2023 23:48:31 GMT
ADD file:54a716f17b23e4fa49d1d5c0a7f63becc295873c116d19bb4753d34f1ca6affb in / 
# Mon, 12 Jun 2023 23:48:31 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 23:50:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 14 Jun 2023 23:50:59 GMT
ENV GOSU_VERSION=1.16
# Wed, 14 Jun 2023 23:51:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jun 2023 23:53:35 GMT
ENV REDIS_VERSION=7.0.11
# Wed, 14 Jun 2023 23:53:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.11.tar.gz
# Wed, 14 Jun 2023 23:53:36 GMT
ENV REDIS_DOWNLOAD_SHA=ce250d1fba042c613de38a15d40889b78f7cb6d5461a27e35017ba39b07221e3
# Wed, 14 Jun 2023 23:55:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 14 Jun 2023 23:55:16 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 14 Jun 2023 23:55:16 GMT
VOLUME [/data]
# Wed, 14 Jun 2023 23:55:17 GMT
WORKDIR /data
# Wed, 14 Jun 2023 23:55:17 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 14 Jun 2023 23:55:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 23:55:18 GMT
EXPOSE 6379
# Wed, 14 Jun 2023 23:55:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:70c60174b18d99741c33011138b5abf2f4d8eca0384521ccb43db3612078e36f`  
		Last Modified: Mon, 12 Jun 2023 23:51:26 GMT  
		Size: 27.0 MB (26982142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453426d1f282966dffaa1cdcee0c63c92cfcb70aede298b04bc41fc37f703174`  
		Last Modified: Wed, 14 Jun 2023 23:59:05 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ddc8babbbac0cb2858c5396dbce34c597d24aa9b5c3bd001fa14000e8c880c`  
		Last Modified: Wed, 14 Jun 2023 23:59:05 GMT  
		Size: 1.4 MB (1413746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafd64461d3cdad052ed43b5ea65a50d8ab573ac83f5a2a107cac696fd4937e7`  
		Last Modified: Wed, 14 Jun 2023 23:59:23 GMT  
		Size: 15.9 MB (15868504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fb0be79ea47ad543019a14ff3181d6ac9d9eab9f8dcfa28fe32b2413c50c6e`  
		Last Modified: Wed, 14 Jun 2023 23:59:20 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978681d3427c16db328c9addec4b1161b596790b4d3472aaa054898a98c26783`  
		Last Modified: Wed, 14 Jun 2023 23:59:20 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:02f48bad3678cba7ef08f68f83b266d26a20c0fe042725bcd8a684365ea6e225
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47045023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f5d0b64daf7f45bb302346a9cb8a5a86f1d29bb45de6384540bbe51f4cf788`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 21:50:14 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 14 Jun 2023 21:50:14 GMT
ENV GOSU_VERSION=1.16
# Wed, 14 Jun 2023 21:50:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jun 2023 21:52:03 GMT
ENV REDIS_VERSION=7.0.11
# Wed, 14 Jun 2023 21:52:03 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.11.tar.gz
# Wed, 14 Jun 2023 21:52:03 GMT
ENV REDIS_DOWNLOAD_SHA=ce250d1fba042c613de38a15d40889b78f7cb6d5461a27e35017ba39b07221e3
# Wed, 14 Jun 2023 21:52:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 14 Jun 2023 21:52:42 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 14 Jun 2023 21:52:42 GMT
VOLUME [/data]
# Wed, 14 Jun 2023 21:52:42 GMT
WORKDIR /data
# Wed, 14 Jun 2023 21:52:43 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:52:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:52:43 GMT
EXPOSE 6379
# Wed, 14 Jun 2023 21:52:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1759dbde33aa972cbcf138cba603f858cf627f00c4007f4a49183c1de2c85f34`  
		Last Modified: Wed, 14 Jun 2023 21:56:22 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c302c4311d2e0ea61eedbcc3e2b4f8743076e32323d0076166e84f2721aa0c7`  
		Last Modified: Wed, 14 Jun 2023 21:56:23 GMT  
		Size: 1.4 MB (1368131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d78a60c5fcd285ac9d54cb03c351f1d7690ef3bf37ef853ee3e29ce047ba62`  
		Last Modified: Wed, 14 Jun 2023 21:56:53 GMT  
		Size: 16.5 MB (16522531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad510f4863eed3df42896129bb948149e0f77a3352ccfc5858c6c85653085d0b`  
		Last Modified: Wed, 14 Jun 2023 21:56:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0fd2612b38ae8a22c9bb115fa1662307513f04e0b5c069156911552d93cc0c`  
		Last Modified: Wed, 14 Jun 2023 21:56:50 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:15a3e0e89db9c6de7f6988449b959d6337e946bbad9f40c49c206c4dfeb3f4f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52796282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42c96ed543fabdacf2393945eec9a85971d8f7d47b5d30cf77d76ad216a0a88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:34 GMT
ADD file:3f8b9849acb625537f99921ef80190de7b03afdc287a5d1113a92cc41ae24be2 in / 
# Mon, 12 Jun 2023 23:17:36 GMT
CMD ["bash"]
# Thu, 15 Jun 2023 00:01:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Thu, 15 Jun 2023 00:01:30 GMT
ENV GOSU_VERSION=1.16
# Thu, 15 Jun 2023 00:01:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 15 Jun 2023 00:03:56 GMT
ENV REDIS_VERSION=7.0.11
# Thu, 15 Jun 2023 00:03:56 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.11.tar.gz
# Thu, 15 Jun 2023 00:03:56 GMT
ENV REDIS_DOWNLOAD_SHA=ce250d1fba042c613de38a15d40889b78f7cb6d5461a27e35017ba39b07221e3
# Thu, 15 Jun 2023 00:05:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Thu, 15 Jun 2023 00:05:27 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Jun 2023 00:05:28 GMT
VOLUME [/data]
# Thu, 15 Jun 2023 00:05:28 GMT
WORKDIR /data
# Thu, 15 Jun 2023 00:05:28 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Thu, 15 Jun 2023 00:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:05:29 GMT
EXPOSE 6379
# Thu, 15 Jun 2023 00:05:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9f041b53cef30007c43057f2520876c85ed6bee6be5aaee867dfb31a053d6cca`  
		Last Modified: Mon, 12 Jun 2023 23:24:09 GMT  
		Size: 33.1 MB (33116725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaeea97777e51880a06577044a03e92b5965f90da1ddc2863e8f697b4576dd2d`  
		Last Modified: Thu, 15 Jun 2023 00:09:23 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f38f4b2d8bfe94cb11897867dbff358f25abeee00747177cd7b8895cd8a5a71`  
		Last Modified: Thu, 15 Jun 2023 00:09:24 GMT  
		Size: 1.4 MB (1359285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ff1c126aac8b47651c89bff16a679a9d913e8c06c260c8cb883ed01a7e538c`  
		Last Modified: Thu, 15 Jun 2023 00:09:49 GMT  
		Size: 18.3 MB (18318441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daedbabbee0fc031cf5fa140e44a4794afe2cdb2d77397896f1fb3a3f3afb0d`  
		Last Modified: Thu, 15 Jun 2023 00:09:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c0b4d8a13b056470c76dd6601540ce545c11791a41ac03ffbf891052a7ac1`  
		Last Modified: Thu, 15 Jun 2023 00:09:44 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
