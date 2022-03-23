## `memcached:alpine3.15`

```console
$ docker pull memcached@sha256:15f87313e52f2c53de4c23a040a0c2fe4a30617e2e3521ad1570a4f24327c0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:alpine3.15` - linux; amd64

```console
$ docker pull memcached@sha256:f5feb2873352ae0a79d0a405c711c15a8a585184884b9f091bbceaa44644fcdc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3862515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f65d290cd47e2644dd3ea539c6a85395be0a8874ea96e77a3f0f7476c400d6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:54:06 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 23 Mar 2022 17:54:07 GMT
RUN apk add --no-cache libsasl
# Wed, 23 Mar 2022 17:54:07 GMT
ENV MEMCACHED_VERSION=1.6.14
# Wed, 23 Mar 2022 17:54:07 GMT
ENV MEMCACHED_SHA1=be64c11d34f04bd1855100b8b5ad9ae8b45e0ab0
# Wed, 23 Mar 2022 17:57:59 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 23 Mar 2022 17:57:59 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 23 Mar 2022 17:57:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 23 Mar 2022 17:57:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 17:57:59 GMT
USER memcache
# Wed, 23 Mar 2022 17:57:59 GMT
EXPOSE 11211
# Wed, 23 Mar 2022 17:58:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf8bd4879a6cfa46efebef4b4001d277e6fb7722c476791ba3257fdc7e81324`  
		Last Modified: Wed, 23 Mar 2022 17:58:33 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def77fcdbc2fc69bedd657126fb234cb4245b81a79be3fe11aa67973cdb4eb51`  
		Last Modified: Wed, 23 Mar 2022 17:58:33 GMT  
		Size: 109.2 KB (109167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14365ef6299a10d8a15cb16261d074f256e4331b8fe32d0ea15980ffc63fb26`  
		Last Modified: Wed, 23 Mar 2022 17:58:33 GMT  
		Size: 939.0 KB (938987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7a217b2b6e0644da93e1a1524dfc72023b73d8b5e95a6949645706db5fbedf`  
		Last Modified: Wed, 23 Mar 2022 17:58:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39f8095de1187212e225d537fab816f30cdc38c67c6d44781bbe3799d72408c`  
		Last Modified: Wed, 23 Mar 2022 17:58:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:095e0c44c122b636ae053f2971bb454b3edfe210195707983a9e0a38d22f4411
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01922b70bc4d8d1d2be9eabafa82a0f0152a88e5871b7e9b6949cf1327c9c4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 11:39:00 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Mar 2022 11:39:02 GMT
RUN apk add --no-cache libsasl
# Thu, 17 Mar 2022 11:39:03 GMT
ENV MEMCACHED_VERSION=1.6.14
# Thu, 17 Mar 2022 11:39:04 GMT
ENV MEMCACHED_SHA1=be64c11d34f04bd1855100b8b5ad9ae8b45e0ab0
# Thu, 17 Mar 2022 11:41:43 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Mar 2022 11:41:45 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Mar 2022 11:41:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 11:41:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 11:41:47 GMT
USER memcache
# Thu, 17 Mar 2022 11:41:48 GMT
EXPOSE 11211
# Thu, 17 Mar 2022 11:41:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33dde588ab12fbb6aa46070a960ac850c8347e86f29744b40a123a466d4885ab`  
		Last Modified: Thu, 17 Mar 2022 11:42:57 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdeb7ac9fd9c67010a55bf3fe0e13866bb31d847353f455c95220027e2bc48c`  
		Last Modified: Thu, 17 Mar 2022 11:42:58 GMT  
		Size: 110.6 KB (110556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bf3828467e4d3c16fcdc94bf5987db023e892ef9594c9c5dc2c3ccf07bc4bc`  
		Last Modified: Thu, 17 Mar 2022 11:42:58 GMT  
		Size: 927.5 KB (927550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e5be11e10e43e4991c6d85f4bdce89416e75c908d33656e4dcb79c26a51bc`  
		Last Modified: Thu, 17 Mar 2022 11:42:57 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9404edf07c113d954a0a5c34650b52d9a1f8e57d166b3e1b022a82c3e27e724`  
		Last Modified: Thu, 17 Mar 2022 11:42:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.15` - linux; 386

```console
$ docker pull memcached@sha256:8a6352e717a8080f0c0888560cf7ae52c77ee2cbd10ed46c68822370b5188d0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db903b8d549ba5f131fc35c81b69bdf1822950956033492f126e16dd95b5750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 17 Mar 2022 08:13:03 GMT
ADD file:22216bc654d9177244235f242fa83cae3b283b3c145cad7ccf11c0d29f5f0ff2 in / 
# Thu, 17 Mar 2022 08:13:03 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 17:35:31 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Mar 2022 17:35:32 GMT
RUN apk add --no-cache libsasl
# Thu, 17 Mar 2022 17:35:32 GMT
ENV MEMCACHED_VERSION=1.6.14
# Thu, 17 Mar 2022 17:35:33 GMT
ENV MEMCACHED_SHA1=be64c11d34f04bd1855100b8b5ad9ae8b45e0ab0
# Thu, 17 Mar 2022 17:39:25 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Mar 2022 17:39:25 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Mar 2022 17:39:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 17:39:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 17:39:26 GMT
USER memcache
# Thu, 17 Mar 2022 17:39:26 GMT
EXPOSE 11211
# Thu, 17 Mar 2022 17:39:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93317a1f65ec94b67aefe728a598022610246404e3a68d391c76cd0e5244a2a0`  
		Last Modified: Thu, 17 Mar 2022 08:13:56 GMT  
		Size: 2.8 MB (2821789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d8e906564040308eb9f4b96b3808d37aa02b7fffa8e8d5c80126d5e50b1cf`  
		Last Modified: Thu, 17 Mar 2022 17:40:52 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16143ebb273f49cf3884d5a063dfac8b30d9527c5018e90fac51ac381b5a5f8b`  
		Last Modified: Thu, 17 Mar 2022 17:40:52 GMT  
		Size: 121.2 KB (121183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107340d48cdbc30d4b57291ca0d28997feed13517f3a508b3b398620dbc97099`  
		Last Modified: Thu, 17 Mar 2022 17:40:52 GMT  
		Size: 947.1 KB (947068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a791ada3ee704cad0a4dba90d29f533e6fcadb132c2522c38b4f0680201a86a9`  
		Last Modified: Thu, 17 Mar 2022 17:40:52 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc23e842aa74aed8a4ea48cf2b6f027f9592e43e117c394bc70b3d2dcf0627c`  
		Last Modified: Thu, 17 Mar 2022 17:40:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.15` - linux; ppc64le

```console
$ docker pull memcached@sha256:02301ceeb8db84476d6a830e0eb4a0bd74985b3b924e06ccc52b3f13bddbf547
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3907497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915198e5de0e2ec569e2410ce30dfe397bccf967b53ad8cbb7fd7776e0cb31c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 17 Mar 2022 11:14:04 GMT
ADD file:ddc94e1e084c05807db26adcc95b47a137fa47fb391e75998b338ada65e00c1c in / 
# Thu, 17 Mar 2022 11:14:09 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 01:40:49 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 18 Mar 2022 01:41:02 GMT
RUN apk add --no-cache libsasl
# Fri, 18 Mar 2022 01:41:07 GMT
ENV MEMCACHED_VERSION=1.6.14
# Fri, 18 Mar 2022 01:41:11 GMT
ENV MEMCACHED_SHA1=be64c11d34f04bd1855100b8b5ad9ae8b45e0ab0
# Fri, 18 Mar 2022 01:44:23 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 18 Mar 2022 01:44:25 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 18 Mar 2022 01:44:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 01:44:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 01:44:48 GMT
USER memcache
# Fri, 18 Mar 2022 01:44:53 GMT
EXPOSE 11211
# Fri, 18 Mar 2022 01:44:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eef85fcc847498263d979ef7ec75680d05e90815eb83a9ec4db135b990c0d8b8`  
		Last Modified: Thu, 17 Mar 2022 11:15:15 GMT  
		Size: 2.8 MB (2814051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d9a8bcef701af3b486b876d321abf97b3658c1167be8849897ceda7cf6f7fa`  
		Last Modified: Fri, 18 Mar 2022 01:46:45 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d22440a9b52437d61f27244ea347af2ab64e01456817e5c7cb34b2eb0b072`  
		Last Modified: Fri, 18 Mar 2022 01:46:45 GMT  
		Size: 126.3 KB (126258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6694bd1424f2bd2ce823b6ba4794da7eb5636331c7dc0f3b8a9425df6de54307`  
		Last Modified: Fri, 18 Mar 2022 01:46:45 GMT  
		Size: 965.5 KB (965511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104fb11e4cec7c5dda13dda5a6d888f9bd2ebcd61e6a2efa8b0e6830d8c0a654`  
		Last Modified: Fri, 18 Mar 2022 01:46:45 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2a08296942faafbbc3900c790682e9743dd251eab462c1797b0e8ecdf6b531`  
		Last Modified: Fri, 18 Mar 2022 01:46:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.15` - linux; s390x

```console
$ docker pull memcached@sha256:5a931719c887b04ccf389c14867075cca4a76c774ecceb8231f801d876c94be9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3651372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aed3255f32676856491e1f6e999893205a57c1d26f36d52518c7d72433bcd9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 17 Mar 2022 03:04:28 GMT
ADD file:f623c69acb1859b41ef29e8f20f4e6c7072d9c6d7210d745afc615251bfe418f in / 
# Thu, 17 Mar 2022 03:04:28 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:51:10 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Mar 2022 08:51:11 GMT
RUN apk add --no-cache libsasl
# Thu, 17 Mar 2022 08:51:12 GMT
ENV MEMCACHED_VERSION=1.6.14
# Thu, 17 Mar 2022 08:51:12 GMT
ENV MEMCACHED_SHA1=be64c11d34f04bd1855100b8b5ad9ae8b45e0ab0
# Thu, 17 Mar 2022 08:54:42 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Mar 2022 08:54:42 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Mar 2022 08:54:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 08:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 08:54:43 GMT
USER memcache
# Thu, 17 Mar 2022 08:54:44 GMT
EXPOSE 11211
# Thu, 17 Mar 2022 08:54:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d51040c5bfbf434887bfed2557335a411e6ef760d04cc178d455d1c3ec1b721c`  
		Last Modified: Thu, 17 Mar 2022 03:05:26 GMT  
		Size: 2.6 MB (2601715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafa61f6f0948b111a53b71e2c8c1312981357779ca88eaf5e60d4163dc7d03b`  
		Last Modified: Thu, 17 Mar 2022 08:55:51 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6282933aed68188fd9995db64b18a466643f4879e98a97392e6df0309f825ab`  
		Last Modified: Thu, 17 Mar 2022 08:55:51 GMT  
		Size: 113.8 KB (113794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d266558ba8144540d874cf2a04b80cdad0b98138893dbd2bf8dfc0a82587d0fc`  
		Last Modified: Thu, 17 Mar 2022 08:55:51 GMT  
		Size: 934.2 KB (934189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97cc0f7d043b7a30a2ecd4a02847ed3d1227cdec67c577b9486ae3a40bb7f55`  
		Last Modified: Thu, 17 Mar 2022 08:55:51 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973434578ea89c81d5ee8f8c926d6efab348a190b4d1f8c59c32b595e5e3ff14`  
		Last Modified: Thu, 17 Mar 2022 08:55:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
