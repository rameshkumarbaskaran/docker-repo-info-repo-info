## `redis:rc-32bit-buster`

```console
$ docker pull redis@sha256:1bec69241021b062ddfffd7866a55817d894d7b9fd8e359a78933322668029f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:rc-32bit-buster` - linux; amd64

```console
$ docker pull redis@sha256:68e3031e5f42820afcdcf4d30cefe50cc7a83f23d9a901291d04decce8f483fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41212602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16236e73ef08740d3d02e5705a240bc17e13b2df1294239fc3b1b4678095385`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sun, 29 Dec 2019 00:04:37 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sun, 29 Dec 2019 00:04:37 GMT
ENV GOSU_VERSION=1.11
# Sun, 29 Dec 2019 00:04:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 29 Dec 2019 00:04:50 GMT
ENV REDIS_VERSION=6.0-rc1
# Sun, 29 Dec 2019 00:04:50 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc1.tar.gz
# Sun, 29 Dec 2019 00:04:51 GMT
ENV REDIS_DOWNLOAD_SHA=2676012e2fcfe8d41e594b2ae8a05d0a050d2d84c38a0471ae5fe0143e4b0eca
# Sun, 29 Dec 2019 00:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends libc6-i386; 	rm -rf /var/lib/apt/lists/*
# Sun, 29 Dec 2019 00:07:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sun, 29 Dec 2019 00:07:24 GMT
RUN mkdir /data && chown redis:redis /data
# Sun, 29 Dec 2019 00:07:24 GMT
VOLUME [/data]
# Sun, 29 Dec 2019 00:07:24 GMT
WORKDIR /data
# Sun, 29 Dec 2019 00:07:25 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sun, 29 Dec 2019 00:07:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 29 Dec 2019 00:07:25 GMT
EXPOSE 6379
# Sun, 29 Dec 2019 00:07:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da01136793fac089b2ff13c2bf3c9d5d5550420fbd9981e08198fd251a0ab7b4`  
		Last Modified: Sun, 29 Dec 2019 00:12:36 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1486a2c0b86ddb45238e86c6bf9666c20113f7878e4cd4fa175fd74ac5d5b7`  
		Last Modified: Sun, 29 Dec 2019 00:12:37 GMT  
		Size: 1.4 MB (1357602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf88906de0fcc88313b8c064bf3e9963678988cc06f25060102c79e76be3861e`  
		Last Modified: Sun, 29 Dec 2019 00:12:44 GMT  
		Size: 5.3 MB (5295578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45923ec9d81deffc1e8af1ca91fc7a44d6e1d76ff127e20f5a44f59cb5065b37`  
		Last Modified: Sun, 29 Dec 2019 00:12:45 GMT  
		Size: 7.5 MB (7464910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec40236ae401206d262b728a0a747dc9b734a4f53685b3e3a3310d5204b5ee11`  
		Last Modified: Sun, 29 Dec 2019 00:12:44 GMT  
		Size: 97.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae55cb5eb99387c92034faa136b490de3a87f88cbc12a11ddec5d2c1fe4d00e`  
		Last Modified: Sun, 29 Dec 2019 00:12:43 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
