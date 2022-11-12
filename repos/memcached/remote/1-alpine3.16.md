## `memcached:1-alpine3.16`

```console
$ docker pull memcached@sha256:4828ace12ebcedaea6787669846e07d19361491cf0466bcd5e523554d1973cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine3.16` - linux; amd64

```console
$ docker pull memcached@sha256:a6a67c90a8ed59d783ffe08e92ae64a31234cd8419f7e833390df717f576ecdb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3868441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b233956ba3849ec7a51524db5011b4cf01ae5c2ac9f9f466904c5db1e293763e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:04:22 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 06 Oct 2022 23:04:23 GMT
RUN apk add --no-cache libsasl
# Thu, 06 Oct 2022 23:04:23 GMT
ENV MEMCACHED_VERSION=1.6.17
# Thu, 06 Oct 2022 23:04:23 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Thu, 06 Oct 2022 23:07:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 06 Oct 2022 23:07:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 06 Oct 2022 23:07:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Oct 2022 23:07:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:07:05 GMT
USER memcache
# Thu, 06 Oct 2022 23:07:06 GMT
EXPOSE 11211
# Thu, 06 Oct 2022 23:07:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05043c369d69c009735a15a9744436e23146b77cbe1a26c2ed0f5616a661f10`  
		Last Modified: Thu, 06 Oct 2022 23:07:34 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efed45ef529d4d67fd065c84fcabccff2894b6bcc32a9784397e7fba3250a9`  
		Last Modified: Thu, 06 Oct 2022 23:07:34 GMT  
		Size: 108.3 KB (108322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb4294ac47814ce133dd818df8f63af0a0797c2841f5b0a68082756dbeb912`  
		Last Modified: Thu, 06 Oct 2022 23:07:35 GMT  
		Size: 952.4 KB (952391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741860cd66bb4504aa36a938ba8b828510cb649a74c3033a83483bfd286ba6c3`  
		Last Modified: Thu, 06 Oct 2022 23:07:34 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb255c1879ff3807f6fb2838ecb5f6a383239ee49799fe9461b873027266d7`  
		Last Modified: Thu, 06 Oct 2022 23:07:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:71cc45cccf702b61190398b6a87642f5b2af94f4c35c77ad3a091f2392b31345
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e852d2c8040bca8153e94c2022fe86782aa0cbac8fc801123ca0b3e0863b455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:32:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Sat, 12 Nov 2022 04:32:00 GMT
RUN apk add --no-cache libsasl
# Sat, 12 Nov 2022 04:32:00 GMT
ENV MEMCACHED_VERSION=1.6.17
# Sat, 12 Nov 2022 04:32:00 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Sat, 12 Nov 2022 04:34:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Sat, 12 Nov 2022 04:34:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 12 Nov 2022 04:34:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 12 Nov 2022 04:34:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:34:47 GMT
USER memcache
# Sat, 12 Nov 2022 04:34:47 GMT
EXPOSE 11211
# Sat, 12 Nov 2022 04:34:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0166ddad77ca75f8f7576619e030ddc2811f9cb7019795c6f313cb8579d7d3da`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d22178c258aa504d67b140d67b44bcbcac169b1c2be5ba239d967ecc0c65b`  
		Last Modified: Sat, 12 Nov 2022 04:35:12 GMT  
		Size: 109.7 KB (109673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36224bcca30debf6e43c90456e7caf05e7579442550546337686055217ac8d4`  
		Last Modified: Sat, 12 Nov 2022 04:35:12 GMT  
		Size: 940.0 KB (940006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a839705f1a3bfe0d8449d3c5af67612e127568f9c047eec3902c7bd1ab5ed9a`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3310158c7f98be809a2f959aa3ec8b84d01e817dfb25821aaedc2086b1bbc05f`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; 386

```console
$ docker pull memcached@sha256:37d7600a73d7da38c974fc706e77404017c11b95cb9c38535949b24658ee1a2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3892679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff894a55a10a668868e6a5c5730bf58c4bc9ae13318f7102835ff27a1ceda7ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:36:27 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Sat, 12 Nov 2022 04:36:29 GMT
RUN apk add --no-cache libsasl
# Sat, 12 Nov 2022 04:36:29 GMT
ENV MEMCACHED_VERSION=1.6.17
# Sat, 12 Nov 2022 04:36:30 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Sat, 12 Nov 2022 04:39:35 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Sat, 12 Nov 2022 04:39:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 12 Nov 2022 04:39:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 12 Nov 2022 04:39:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:39:39 GMT
USER memcache
# Sat, 12 Nov 2022 04:39:40 GMT
EXPOSE 11211
# Sat, 12 Nov 2022 04:39:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9951891b1310ad820489c84181ff9abc7a586b81689546580b16f189094d41d1`  
		Last Modified: Sat, 12 Nov 2022 04:40:32 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a4db546c4d6c4868971c26bad4fdd8c23c2905b85b298e510703801325aec7`  
		Last Modified: Sat, 12 Nov 2022 04:40:33 GMT  
		Size: 119.8 KB (119850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3191a52cde04cecccbdca0349040db5676d8b35445d4679762ff7769a2d6d0c1`  
		Last Modified: Sat, 12 Nov 2022 04:40:33 GMT  
		Size: 962.8 KB (962833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ea727b4b388cb040e6456cdba2d85820f68dff59247e797677f5a10f926f26`  
		Last Modified: Sat, 12 Nov 2022 04:40:32 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577fc1e88a6f81d9930b42ab5e53354c87a41b5049342da8671161947cb291b`  
		Last Modified: Sat, 12 Nov 2022 04:40:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; ppc64le

```console
$ docker pull memcached@sha256:81d546bacfd81203cb3c139b0f27904589a90a03fd53b984e02dc5698791ce9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3911485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8841333afe5e658648b942d8ff67f5084232bbdb5b08c6587673b6926975b2f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:16:05 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Sat, 12 Nov 2022 05:16:08 GMT
RUN apk add --no-cache libsasl
# Sat, 12 Nov 2022 05:16:08 GMT
ENV MEMCACHED_VERSION=1.6.17
# Sat, 12 Nov 2022 05:16:08 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Sat, 12 Nov 2022 05:22:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Sat, 12 Nov 2022 05:22:48 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 12 Nov 2022 05:22:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 12 Nov 2022 05:22:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 05:22:50 GMT
USER memcache
# Sat, 12 Nov 2022 05:22:50 GMT
EXPOSE 11211
# Sat, 12 Nov 2022 05:22:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39bd7d8ef2d92339bd013519d71e412c48194c541e2d8189e61f7f5e0e52696`  
		Last Modified: Sat, 12 Nov 2022 05:23:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e3d2cb65ba0c78b7e0fa6d9f69c9436d5725b4d358f2b3bbd42e0c776c4205`  
		Last Modified: Sat, 12 Nov 2022 05:23:50 GMT  
		Size: 126.2 KB (126247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe5b6250391fd83411a7f7f7e26933522d3d4cf176b27f1ce74881bdfe65571`  
		Last Modified: Sat, 12 Nov 2022 05:23:51 GMT  
		Size: 982.0 KB (982016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f840b2979b7a4af757216f85b38bf597b65aec22c4c0a52fc2a485923603ae4`  
		Last Modified: Sat, 12 Nov 2022 05:23:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41a55353ca2d3b11b3cd6c6970c7518b076599e6e5173fe78cff19aabda5ed3`  
		Last Modified: Sat, 12 Nov 2022 05:23:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; s390x

```console
$ docker pull memcached@sha256:f54434eb3a66346ad64bbb863fbd3154a5f933626929a48b57039facdc62e314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3647534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdebbb5e0461ebd358c95951b378e4248a7358c25f950bbea3288281ee1e58a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:41:34 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Sat, 12 Nov 2022 04:41:36 GMT
RUN apk add --no-cache libsasl
# Sat, 12 Nov 2022 04:41:37 GMT
ENV MEMCACHED_VERSION=1.6.17
# Sat, 12 Nov 2022 04:41:37 GMT
ENV MEMCACHED_SHA1=e25639473e15f1bd9516b915fb7e03ab8209030f
# Sat, 12 Nov 2022 04:45:35 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Sat, 12 Nov 2022 04:45:36 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 12 Nov 2022 04:45:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 12 Nov 2022 04:45:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:45:39 GMT
USER memcache
# Sat, 12 Nov 2022 04:45:39 GMT
EXPOSE 11211
# Sat, 12 Nov 2022 04:45:40 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc8b46e8fcff953b0e7264a00a6a3aaddbb3587f7e687ad085948e4719ac9ec`  
		Last Modified: Sat, 12 Nov 2022 04:46:39 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef6922364f4028fe814650a91f62dbb38d8610ed1d295e485aa968573dd3b8b`  
		Last Modified: Sat, 12 Nov 2022 04:46:39 GMT  
		Size: 112.5 KB (112517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee3cda70ba8710c5421d518c54a547ed403bb5dc39a9d403d3b095ac8a522d7`  
		Last Modified: Sat, 12 Nov 2022 04:46:39 GMT  
		Size: 942.2 KB (942219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ba4443b0388923438031a6ad05cc470a8ed57fb11923792c112713b33e775c`  
		Last Modified: Sat, 12 Nov 2022 04:46:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d15d1a529e09947f4f27f7d75a09d892dab585782ad766bc691158d3f27ff0`  
		Last Modified: Sat, 12 Nov 2022 04:46:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
