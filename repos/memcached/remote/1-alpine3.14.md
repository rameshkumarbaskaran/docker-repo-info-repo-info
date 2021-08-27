## `memcached:1-alpine3.14`

```console
$ docker pull memcached@sha256:a40ebe0d5276e0f8e6fbe90a119df4239bd8286c8055e2677acef9a852b8193f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine3.14` - linux; amd64

```console
$ docker pull memcached@sha256:34b1ab627355edd9cceaa422b7b91e57caf007ae9b1a22922c38a08660e81efb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3903170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def8a42f3e88882c2265cc9e3f62e9e7681e163fe20a5f403d6fef77e8fb2111`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 07 Aug 2021 00:14:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Sat, 07 Aug 2021 00:14:13 GMT
RUN apk add --no-cache libsasl
# Sat, 07 Aug 2021 00:14:13 GMT
ENV MEMCACHED_VERSION=1.6.10
# Sat, 07 Aug 2021 00:14:14 GMT
ENV MEMCACHED_SHA1=cb5b9fe77a2a59cc6cc7103a415bc07df9ddc6ec
# Sat, 07 Aug 2021 00:18:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Sat, 07 Aug 2021 00:18:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 07 Aug 2021 00:18:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 07 Aug 2021 00:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Aug 2021 00:18:05 GMT
USER memcache
# Sat, 07 Aug 2021 00:18:06 GMT
EXPOSE 11211
# Sat, 07 Aug 2021 00:18:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aeb0b192a3f1081390d942a614d2b614c78be8c6728490b30f3abd0ea9b95a`  
		Last Modified: Sat, 07 Aug 2021 00:18:44 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4abbd93452bbb7ca5339028c20945da9101602ba49f9f42965452a3db6a98d2`  
		Last Modified: Sat, 07 Aug 2021 00:18:43 GMT  
		Size: 155.5 KB (155516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c472ac5a156e0c1551a6f99d1b657a6d495496b0cff418dffc1bbd630bd36640`  
		Last Modified: Sat, 07 Aug 2021 00:18:44 GMT  
		Size: 933.0 KB (932979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d28fec27cb7828cc4877db15d8023b453fef8d557721a6dc2c9f721c801bb`  
		Last Modified: Sat, 07 Aug 2021 00:18:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef85351ee7d962d3acc985da8128513818c7604be17e847251f543dfddf68747`  
		Last Modified: Sat, 07 Aug 2021 00:18:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:3d93273af96de43b51add0d01ffec6cb248a83a6b4adf02cc9e6051b3f96fbd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1be9ff405513cf815b965422761dd197bd3f72229bb2973ea006961381a309`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:44:13 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 06 Aug 2021 19:44:14 GMT
RUN apk add --no-cache libsasl
# Fri, 06 Aug 2021 19:44:14 GMT
ENV MEMCACHED_VERSION=1.6.10
# Fri, 06 Aug 2021 19:44:15 GMT
ENV MEMCACHED_SHA1=cb5b9fe77a2a59cc6cc7103a415bc07df9ddc6ec
# Fri, 06 Aug 2021 19:48:06 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 06 Aug 2021 19:48:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:48:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 06 Aug 2021 19:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:48:08 GMT
USER memcache
# Fri, 06 Aug 2021 19:48:08 GMT
EXPOSE 11211
# Fri, 06 Aug 2021 19:48:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e7ec193b32b8cfc53263af4e876a7055d4318058e76620bce0544f9120c6c7`  
		Last Modified: Fri, 06 Aug 2021 19:49:06 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2047017486a2b18ef6819325e63c7b73faa11404da5ac0addfeeaa66c34d35`  
		Last Modified: Fri, 06 Aug 2021 19:49:06 GMT  
		Size: 157.2 KB (157197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d96bbd7be8b6283902f7bac12c1e45e0cf356d8b8d1c57e298f2df6946aed0d`  
		Last Modified: Fri, 06 Aug 2021 19:49:07 GMT  
		Size: 922.5 KB (922540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7159339c1b34149bc53211472fa2171a492cfcac24ae0584d0e5b8743700edd7`  
		Last Modified: Fri, 06 Aug 2021 19:49:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe1a76a68267bbc6ec790cb0ee914959f9afc0a827978dfc8e5b637dc7a76bc`  
		Last Modified: Fri, 06 Aug 2021 19:49:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.14` - linux; 386

```console
$ docker pull memcached@sha256:82a99c470435ce9fd7cebf6565305c9f9a20eb2142839f8a7eaf42fc04b1e64a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503d28ddbe03b1e33458c354e3e0cef3142579c20bdf6e8c1f4b447257a2de01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:48:52 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 27 Aug 2021 19:48:54 GMT
RUN apk add --no-cache libsasl
# Fri, 27 Aug 2021 19:48:54 GMT
ENV MEMCACHED_VERSION=1.6.10
# Fri, 27 Aug 2021 19:48:55 GMT
ENV MEMCACHED_SHA1=cb5b9fe77a2a59cc6cc7103a415bc07df9ddc6ec
# Fri, 27 Aug 2021 19:53:36 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 27 Aug 2021 19:53:36 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 27 Aug 2021 19:53:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 27 Aug 2021 19:53:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 19:53:38 GMT
USER memcache
# Fri, 27 Aug 2021 19:53:38 GMT
EXPOSE 11211
# Fri, 27 Aug 2021 19:53:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a776c6c02658f2d17623bce57a634d82f2dc8c8bee59f4d90fc786c3e69e31ff`  
		Last Modified: Fri, 27 Aug 2021 19:54:35 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fab8279289e8b7a476ce09017d9bcdb33bccbe04750f2ccba41c0a43f828b16`  
		Last Modified: Fri, 27 Aug 2021 19:54:35 GMT  
		Size: 169.0 KB (169012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c50e3cfd5d1f42d6dd2505b7b02ca2ed14cb53d2199df2bed319e84146d13b`  
		Last Modified: Fri, 27 Aug 2021 19:54:36 GMT  
		Size: 944.4 KB (944446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856e8e8dfa799b89d86a7552466e0b451bc8b8b140b56d53056ea942b82b102`  
		Last Modified: Fri, 27 Aug 2021 19:54:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd1d4e4fe24a075a95e91ec623e250fb1071d34af2ec3a777ceecca3d62ea9f`  
		Last Modified: Fri, 27 Aug 2021 19:54:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.14` - linux; ppc64le

```console
$ docker pull memcached@sha256:5ceda0e184a63631c255d5e5ff48c4c33d99af475ea06afcea6870e37fe19d68
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22db1888d17d2d29920e6a8042ccce4c79e4869f8c5f9c0c23487d8020f9740c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:46:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 06 Aug 2021 21:46:10 GMT
RUN apk add --no-cache libsasl
# Fri, 06 Aug 2021 21:46:13 GMT
ENV MEMCACHED_VERSION=1.6.10
# Fri, 06 Aug 2021 21:46:14 GMT
ENV MEMCACHED_SHA1=cb5b9fe77a2a59cc6cc7103a415bc07df9ddc6ec
# Fri, 06 Aug 2021 21:49:36 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 06 Aug 2021 21:49:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 06 Aug 2021 21:49:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 06 Aug 2021 21:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 21:50:05 GMT
USER memcache
# Fri, 06 Aug 2021 21:50:08 GMT
EXPOSE 11211
# Fri, 06 Aug 2021 21:50:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a0115207f739cf0dadef89d1d4fa84ff382340ab5cfdc1a8c1d53fd2a4e1f`  
		Last Modified: Fri, 06 Aug 2021 21:51:17 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4535061ab98aeabde3c8815eda6ca7c387deddf01744a07f971c91fdbd402077`  
		Last Modified: Fri, 06 Aug 2021 21:51:17 GMT  
		Size: 179.7 KB (179663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c6a8fbed47687965665fabcb41ff9687a30f7a7ca112954c97c1c6e16cfbe`  
		Last Modified: Fri, 06 Aug 2021 21:51:18 GMT  
		Size: 961.3 KB (961265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95052d9a1041312d1404b4b4497de4ed9bf2db25a9b753d19b1a4b6d6d4f15b0`  
		Last Modified: Fri, 06 Aug 2021 21:51:17 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9a71b75e165be41def41b7731961647b9f9b195ecb92da1d88139d5cf77400`  
		Last Modified: Fri, 06 Aug 2021 21:51:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.14` - linux; s390x

```console
$ docker pull memcached@sha256:cebdf9f1ff4ffe7551d4917b4a53e78ac48da41a694a8301fbd92459ebd9f45f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047503017563255821d3a05e00a220624c8698ef1a285eb6a05023ef0c1335e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:13:56 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 27 Aug 2021 19:13:58 GMT
RUN apk add --no-cache libsasl
# Fri, 27 Aug 2021 19:13:59 GMT
ENV MEMCACHED_VERSION=1.6.10
# Fri, 27 Aug 2021 19:13:59 GMT
ENV MEMCACHED_SHA1=cb5b9fe77a2a59cc6cc7103a415bc07df9ddc6ec
# Fri, 27 Aug 2021 19:22:03 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 27 Aug 2021 19:22:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 27 Aug 2021 19:22:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 27 Aug 2021 19:22:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 19:22:06 GMT
USER memcache
# Fri, 27 Aug 2021 19:22:06 GMT
EXPOSE 11211
# Fri, 27 Aug 2021 19:22:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c3123815589d4cfc45a071f344bd0f3ca08ee63a471c2c114af2dece4699a0`  
		Last Modified: Fri, 27 Aug 2021 19:23:06 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25c400e2d4eb8dee97bc754e9e52585af4304ec8cf3121b619bd5756796fb52`  
		Last Modified: Fri, 27 Aug 2021 19:23:06 GMT  
		Size: 161.5 KB (161520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fd541e530a5444852c1a56f01565817097a4b2abec64399dcf4fdd84dfe88`  
		Last Modified: Fri, 27 Aug 2021 19:23:06 GMT  
		Size: 929.3 KB (929257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb82aed96a5a46fb2399db9bf85a3ff9a7ce3de3468fe74285ad84fd557a1ca`  
		Last Modified: Fri, 27 Aug 2021 19:23:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18159f487fe568305c6aaeb29b07af5f859402bb29566a404f9fccbd86bafbf`  
		Last Modified: Fri, 27 Aug 2021 19:23:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
