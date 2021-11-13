## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:2ba3bff27c5f50a36c0193beefe14562853f85a26a5653c596227672962fcaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:24fe0c92221002cf45e29400954b51ec10d21f0a20b1eed1d9887ab6e53228d8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e46401b1abfbd33861cf376fd90c2907f0145664d55d1c8f9fa16125b395f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:52:14 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Sat, 13 Nov 2021 10:52:16 GMT
RUN apk add --no-cache libsasl
# Sat, 13 Nov 2021 10:52:16 GMT
ENV MEMCACHED_VERSION=1.6.12
# Sat, 13 Nov 2021 10:52:16 GMT
ENV MEMCACHED_SHA1=40d43e98f149e13e6c81eee813e6734f23413a01
# Sat, 13 Nov 2021 10:56:28 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		patch 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& wget -O cdefs.patch 'https://github.com/memcached/memcached/commit/7e570c789f4473354461e6eeb8bb7a283df613bf.patch' 	&& patch -p1 --input=cdefs.patch 	&& rm cdefs.patch 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Sat, 13 Nov 2021 10:56:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 13 Nov 2021 10:56:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 13 Nov 2021 10:56:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:56:29 GMT
USER memcache
# Sat, 13 Nov 2021 10:56:29 GMT
EXPOSE 11211
# Sat, 13 Nov 2021 10:56:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dd13c8de54c9c61f3ea2d779bb5bb3c6dc9b55d5357bd18d74574d7bfa179f`  
		Last Modified: Sat, 13 Nov 2021 10:56:57 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed128e2fdfa541f0c77953dc099bf89a5e5ebb0af1876f765e79b6f3ed5fb1d7`  
		Last Modified: Sat, 13 Nov 2021 10:56:58 GMT  
		Size: 156.1 KB (156075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e79216f34c8769a41f87dc086e59cb00f30c4338438c62bbaf7f000cf7debaf`  
		Last Modified: Sat, 13 Nov 2021 10:56:58 GMT  
		Size: 941.1 KB (941121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2081b9b9514a1e372eab42bb7c1ae3ad7944d3dfba055caf8021439bca8f37f2`  
		Last Modified: Sat, 13 Nov 2021 10:56:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5422f709785bad082602079821b8f9240800cf6ec9b9f28ac550bd6d3b46f923`  
		Last Modified: Sat, 13 Nov 2021 10:56:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:79a5646a0c845a791f36017fda3292281b48295b06c53f13d62c9f94237d4731
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afac0e49af3ce3f1769abe11a29f8f5610c6a736d8c5b6c7b9770c8d8e94e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:43:29 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 06:43:31 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 06:43:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 06:43:35 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 06:46:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 06:46:33 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:46:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 06:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:46:36 GMT
USER memcache
# Thu, 17 Dec 2020 06:46:38 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 06:46:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68564bbfc09f153688e942bf54d5375d1e27f3507c0bed6b038c2ac8ce095aa5`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac3a91edee49d0b08a25706ae86059bed89941a08b496e72ef092e57c4ecb3`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16e9bb942ec42a35a792beab65aea843209e7bdde7e856499b9fc85f93bc4e`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.5 MB (1537248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc15394239bd0c083e1b6df806aa5ffeb8b9cc7e80113afc2959721de49f90d1`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482f0eb571548eae5720c652ff7da13558e56a8722dc9932cf7eb1ef3eb33acb`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2320b287d196d58506ce8a59f669406737816c2340166cbcc0f2ab2a0ff08f9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8eafc3982c8814a8ebc74b54435bc52f2561a3f9b651845b6304a3f1ed04b1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:18:29 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Sat, 13 Nov 2021 06:18:31 GMT
RUN apk add --no-cache libsasl
# Sat, 13 Nov 2021 06:18:31 GMT
ENV MEMCACHED_VERSION=1.6.12
# Sat, 13 Nov 2021 06:18:32 GMT
ENV MEMCACHED_SHA1=40d43e98f149e13e6c81eee813e6734f23413a01
# Sat, 13 Nov 2021 06:21:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		patch 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& wget -O cdefs.patch 'https://github.com/memcached/memcached/commit/7e570c789f4473354461e6eeb8bb7a283df613bf.patch' 	&& patch -p1 --input=cdefs.patch 	&& rm cdefs.patch 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Sat, 13 Nov 2021 06:21:21 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 13 Nov 2021 06:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 13 Nov 2021 06:21:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:21:23 GMT
USER memcache
# Sat, 13 Nov 2021 06:21:24 GMT
EXPOSE 11211
# Sat, 13 Nov 2021 06:21:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257dd229206b68e4da8ccb3fd9f080ac07136eb990155a9b3d05e89f8b402d0d`  
		Last Modified: Sat, 13 Nov 2021 06:22:16 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925f34344a0c1c207e49d31bc1a8627e891f91cd0b28c2739d072e4f10a93ce2`  
		Last Modified: Sat, 13 Nov 2021 06:22:16 GMT  
		Size: 157.5 KB (157520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52a38736b9393d4a44db737a88cf6c1831f7d8c74b35c86ff7f9eaf2855cc09`  
		Last Modified: Sat, 13 Nov 2021 06:22:16 GMT  
		Size: 932.4 KB (932428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5243596d29ace43a3a137acf96b48d967faef5ac393b2c223a5174d9c5e0df19`  
		Last Modified: Sat, 13 Nov 2021 06:22:16 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9075017e39dfddff545e122699b6d76464c96c7364b4b9b992baa4b326e1f6ed`  
		Last Modified: Sat, 13 Nov 2021 06:22:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:05a8f320f47594e13a995ce6010bf1a1ffefbc0801af3db71a4b307d80507e1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1e161777c7fd07b94454291643f42ea0fdb356659939cacc64e2c422043bc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:46:45 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Sat, 13 Nov 2021 04:46:49 GMT
RUN apk add --no-cache libsasl
# Sat, 13 Nov 2021 04:46:49 GMT
ENV MEMCACHED_VERSION=1.6.12
# Sat, 13 Nov 2021 04:46:49 GMT
ENV MEMCACHED_SHA1=40d43e98f149e13e6c81eee813e6734f23413a01
# Sat, 13 Nov 2021 04:51:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		patch 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& wget -O cdefs.patch 'https://github.com/memcached/memcached/commit/7e570c789f4473354461e6eeb8bb7a283df613bf.patch' 	&& patch -p1 --input=cdefs.patch 	&& rm cdefs.patch 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Sat, 13 Nov 2021 04:51:34 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 13 Nov 2021 04:51:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 13 Nov 2021 04:51:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 04:51:36 GMT
USER memcache
# Sat, 13 Nov 2021 04:51:36 GMT
EXPOSE 11211
# Sat, 13 Nov 2021 04:51:36 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c46fffe62fb0019a4a07ff2412b24ba768fc0fe1ee896ce405f17a146965e5c`  
		Last Modified: Sat, 13 Nov 2021 04:52:35 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004710d37e9403df71cb3fa6063baaf4004e9418464f8621db5ba29310ff8fb`  
		Last Modified: Sat, 13 Nov 2021 04:52:35 GMT  
		Size: 169.6 KB (169573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9161e4c57fb351a22220501b4c08183033118afcbaa7beef5762a955438349f6`  
		Last Modified: Sat, 13 Nov 2021 04:52:36 GMT  
		Size: 950.1 KB (950052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c312000a267549cfd43968578cd3771463d93a65c3f86374f6b008a35f046a`  
		Last Modified: Sat, 13 Nov 2021 04:52:35 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787bea0271bcbfa90b80bf75b09eaddd3b43df3f3c3921ed539a329e0c597e4e`  
		Last Modified: Sat, 13 Nov 2021 04:52:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0a092ee211f4ca24c5ee4afde3eed73e3e3edafc00740395a4f2b75319f742dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3970089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d32709506fcbe3475a0287966e5bde61b997246d6d150061a9e32dd384091c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:00:02 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Sat, 13 Nov 2021 03:00:21 GMT
RUN apk add --no-cache libsasl
# Sat, 13 Nov 2021 03:00:26 GMT
ENV MEMCACHED_VERSION=1.6.12
# Sat, 13 Nov 2021 03:00:31 GMT
ENV MEMCACHED_SHA1=40d43e98f149e13e6c81eee813e6734f23413a01
# Sat, 13 Nov 2021 03:04:28 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		patch 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& wget -O cdefs.patch 'https://github.com/memcached/memcached/commit/7e570c789f4473354461e6eeb8bb7a283df613bf.patch' 	&& patch -p1 --input=cdefs.patch 	&& rm cdefs.patch 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Sat, 13 Nov 2021 03:04:31 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 13 Nov 2021 03:04:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 13 Nov 2021 03:04:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 03:04:54 GMT
USER memcache
# Sat, 13 Nov 2021 03:04:57 GMT
EXPOSE 11211
# Sat, 13 Nov 2021 03:05:02 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd78e6619b0e75b32b3656af62ad029d0d590ae119d80dff2612c5409f5f0b45`  
		Last Modified: Sat, 13 Nov 2021 03:05:55 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d81240ceb07a14f932db1cfdac081d6c07939ccc383fbd9b602ee947c2dee96`  
		Last Modified: Sat, 13 Nov 2021 03:05:56 GMT  
		Size: 180.2 KB (180174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e322cd1fb16c82653cad349dfe95b2be55a658f7b7f8cadc3bfd90b8de4cb975`  
		Last Modified: Sat, 13 Nov 2021 03:05:56 GMT  
		Size: 970.8 KB (970772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c17fb8d41cea82e2d52a931c43cb9379d9396672f936c419c05ac746b94419`  
		Last Modified: Sat, 13 Nov 2021 03:05:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf37427a12ab0ec1955488c4a6578058b1881c3da559d11b17b7d30dd2d317fc`  
		Last Modified: Sat, 13 Nov 2021 03:05:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1b2bd7c7c893d4619f67803179a8e276ffc71a43d9285193a16a699b98b8f9fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3711542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214865d6870bcf452c58e069ff79305ba4b2d0670fc99c62dfde711f2fe1f1b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:45:38 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 12 Nov 2021 19:45:39 GMT
RUN apk add --no-cache libsasl
# Fri, 12 Nov 2021 19:45:39 GMT
ENV MEMCACHED_VERSION=1.6.12
# Fri, 12 Nov 2021 19:45:39 GMT
ENV MEMCACHED_SHA1=40d43e98f149e13e6c81eee813e6734f23413a01
# Fri, 12 Nov 2021 19:49:10 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		patch 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& wget -O cdefs.patch 'https://github.com/memcached/memcached/commit/7e570c789f4473354461e6eeb8bb7a283df613bf.patch' 	&& patch -p1 --input=cdefs.patch 	&& rm cdefs.patch 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 12 Nov 2021 19:49:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 12 Nov 2021 19:49:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 12 Nov 2021 19:49:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 19:49:11 GMT
USER memcache
# Fri, 12 Nov 2021 19:49:11 GMT
EXPOSE 11211
# Fri, 12 Nov 2021 19:49:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf7f30b9422719880461a2bf0c11b791cd2c39cd96549ae94e24f47f2b53f6b`  
		Last Modified: Fri, 12 Nov 2021 19:50:07 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d94d5bde813a42df71eb6fb8e8918d316b33a2334291130ef9963b2876273c`  
		Last Modified: Fri, 12 Nov 2021 19:50:07 GMT  
		Size: 162.1 KB (162130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d54547e9c754f3f174681baf1cb250677e458b30cd6c8abfe92efb86462ca6`  
		Last Modified: Fri, 12 Nov 2021 19:50:07 GMT  
		Size: 938.5 KB (938461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961c331695dd80b776e321b05cdd1f3b5dd15742277d5977046aa9045aa2fc74`  
		Last Modified: Fri, 12 Nov 2021 19:50:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684bcc0de6b294726cfdd60525d7a30745807a0efed2e899f985009dbfdce8e9`  
		Last Modified: Fri, 12 Nov 2021 19:50:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
