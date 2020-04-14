## `memcached:alpine`

```console
$ docker pull memcached@sha256:debc6484992f1a9a0bed367c4b999d9177e741dcb66a75260c7de899e8c0c1c0
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

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:42f3c2aa162185e3c8bef259444e2211072916dcd0ea1e3a97ebc40063565c82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acce7f7ac2ef3283ff7538edb59d788e12a173e6c988e8142eda78a9d7d465f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 00:40:06 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 00:40:07 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:28:07 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:28:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:36:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:36:25 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:36:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:36:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:36:26 GMT
USER memcache
# Tue, 14 Apr 2020 00:36:26 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:36:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5fb4ad400df404c486089fa4098e9e6bfdb1528c2ee85cbd5614e8a97f1f9a`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb602a49f6f4777651777faab36b80d92a2f1dbe36d865c0cce4e182439c6b5e`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 15.1 KB (15099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2ad92cd017e016358bcdd19608005e61b96f391f551cbf28b7bf893eb08f27`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 1.6 MB (1551900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c68edd2b2740171a4efac506979aa590d59657cda2b828522131128a70e68`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4b5b784c11b1f78e28ec0cee292cd3ab2e91add940930435cbe73099221381`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:2ad889e13d889d0a7bf42350cd8f4de4e63c14a935ed4eca89c15c22b650caf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd4fa55e8dcf85c1736ab25138f0a2299ec97c84043b1a8893798172fcb5ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:15:28 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 23 Mar 2020 23:15:34 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:51:16 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:51:17 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:00:39 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:00:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:00:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:00:42 GMT
USER memcache
# Tue, 14 Apr 2020 00:00:43 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:00:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f329bb895b7588f4de54c119f39a5f656520bc2310d39893460c4398814112d`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bd8017eeb8ecce1d6b238f86b96a1af52d1a9dd44bc0da4c0573f58a7f51a8`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 14.7 KB (14695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1dbd69370c1c1fd0f473abbd0890a314699b93feb4e9a9397ad89e6f4d08e8`  
		Last Modified: Tue, 14 Apr 2020 00:01:00 GMT  
		Size: 1.5 MB (1513938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02da716a305370dd20bed73237b26c6686af6bb314c1730ca4b677e6b192948c`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a3d551b55e52c8a515a9331168aca21b6fa779ec12e67e0212eb263adeebda`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:885837a59ec430a6ce09168e1e112c2489492a777459c2ba3746b6a238834355
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c4e6f16ce766f5ddbdd7e776cbb0a023368705140109b060f31735444a073c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:07 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 23 Mar 2020 22:14:20 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 01:51:27 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 01:51:28 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 04:38:22 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 04:38:26 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 04:38:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 04:38:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 04:38:40 GMT
USER memcache
# Tue, 14 Apr 2020 04:38:41 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 04:38:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae54837c45cf98e10469ba87b255979740486d00d9407bc2fcdf1492469dc04`  
		Last Modified: Mon, 23 Mar 2020 22:42:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1459ca388d9e53a94cbb39e64789568710013f3b46396b24ea0729b570f74403`  
		Last Modified: Mon, 23 Mar 2020 22:42:44 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a86370a05daf8a7199f633c3d466d71b660a3f93796b8506e07f3b5fb767f56`  
		Last Modified: Tue, 14 Apr 2020 04:39:06 GMT  
		Size: 1.4 MB (1393203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d930ea1b6bafe7bab477839d90a0531c0161bcc161ebde11a1cd62574a199db2`  
		Last Modified: Tue, 14 Apr 2020 04:39:11 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbdd34a23f66358cadcfdc0315321e110c9cc36ef737e7b6ff4934236b1267d`  
		Last Modified: Tue, 14 Apr 2020 04:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:08e4eee2dbc1e2589c53c0bbd26363957880c8563d31786d877d09ec516c0fed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0270dfda3dfe68de5b0bb5335b0930004ca3beed72eca0def0c03de87601b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:16:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 05:16:15 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:57:43 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:57:44 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:06:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:06:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:06:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:06:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:07:00 GMT
USER memcache
# Tue, 14 Apr 2020 00:07:01 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:07:02 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1bfe9c2142f88c6e142b39adf7ba4fe722789b650d5a54184ff336826ae16f`  
		Last Modified: Tue, 24 Mar 2020 05:25:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d8154a8d6d9edf61516528f99c62d27eb41f8602571ae30fdf745976e2c6e`  
		Last Modified: Tue, 24 Mar 2020 05:25:35 GMT  
		Size: 15.5 KB (15490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d54c7f7d9fb444dbe1aee28da7f339cfce0f93316d0e44b528e3f0b1c83a1e`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 1.6 MB (1554129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824223b1a0565c7df241643aa6173bcc7f918bd51af6cd082f1c4dd56375a79`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b98391dc8eb3d7e32edcd1175b80a1588f44e5c9c8f93e0d7d35697e93f67fb`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:788ec77b1bd7a21665769b8e4302e8978c324953b48e09aeb17b41e80e20c5f0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7638872a17e59e75a022dc0c1a0a16cbe719fb3b5503003e4a7110ff97fca043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:38:28 GMT
ADD file:99c8234abafd4fa915c0b826eb0e3be0e6aaa7c1e33cb1214ef71a99e9c02e06 in / 
# Mon, 23 Mar 2020 21:38:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 04:55:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 04:55:13 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:24:28 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:24:29 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:33:02 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:33:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:33:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:33:03 GMT
USER memcache
# Tue, 14 Apr 2020 00:33:03 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:33:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43f6a4398e1c9e860dfb5c93d7049ab9eedf814513bd6d07e06077c560303c7a`  
		Last Modified: Mon, 23 Mar 2020 21:38:48 GMT  
		Size: 2.8 MB (2806122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31d073afa8dea3b0bfd6eeb6ebffc6447996f0e9cabebf9d749474ac22cdf2d`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905909a3db778acdf7295903cff6ee7b27263e33facc5982475e7b60831413fc`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 16.1 KB (16146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55f704c4db8d5686c61a7f5dbf01efb54c26f928a4667edb336aa6b26c9931`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 1.6 MB (1648434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df688f5f46cdef50f778015f724036d02ef66baf23dee71b4f2021a38784bc`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e187a846d19d6476ac11efbcb749911f8f31990824f548f8b22ac752a1218a`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3797459b34cdce19dc5c399b9c197be9e7ba49a5f24eb0519aafb09597505922
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4448507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7465343178ddd65e795fcbffde4546ce34a20537d50c03bf12dc86eb96e1e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:21:29 GMT
ADD file:4b35131542b9682214e1c2c72fe3cea215a10e2f775e87befecd80fe2228d5a0 in / 
# Mon, 23 Mar 2020 21:21:32 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 02:24:20 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 02:24:25 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:42:05 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:42:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:50:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:50:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:51:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 00:51:15 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:51:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc1c99f4ba60de0d3ca52dc6855483e24c91884e33df71f502bbff6eb909d9b9`  
		Last Modified: Mon, 23 Mar 2020 21:22:12 GMT  
		Size: 2.8 MB (2820052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50bd2ca891d67079878bf06e36ba609e8528e83369265c92fbd3b03e6e839f1`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4704e4e496c0d18b40f484fc715146c1f427050210b40271112edcf751a698`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a082e2e1ac7786e3860912de8517980c8e08afb1ffa80d05d52240fbb673698`  
		Last Modified: Tue, 14 Apr 2020 00:51:52 GMT  
		Size: 1.6 MB (1610653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1bdbb7103a9b4c5d777d6f23357bc31745b28dba327fa333173e2306e8ba5c`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a958ecfb0c40b2251cf63426a688c563e8432efc39006acc5192e8fe59b23ab`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:7295e677896a531ce8e2f171fde31f721618611720d4c911132736dbc45fa4d3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04146b145e02520ac8848fd057a913852fd6ea8abc933fec317b7fc06010838d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:43 GMT
ADD file:922e12714922ae035a33d6ceb8d2683ad3e454deca21ad02b699db908443342b in / 
# Thu, 23 Jan 2020 16:52:44 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:24:51 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Jan 2020 17:24:52 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 23 Jan 2020 17:24:52 GMT
ENV MEMCACHED_VERSION=1.5.20
# Thu, 23 Jan 2020 17:24:52 GMT
ENV MEMCACHED_SHA1=5d3b5af3ce0a1483d655017db7228bcaeff10d47
# Thu, 23 Jan 2020 17:28:28 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		perl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 23 Jan 2020 17:28:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 23 Jan 2020 17:28:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jan 2020 17:28:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:28:29 GMT
USER memcache
# Thu, 23 Jan 2020 17:28:29 GMT
EXPOSE 11211
# Thu, 23 Jan 2020 17:28:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0449d076b2977b7e7ce4c35b0fe5199d86cabaf453e869da73b2efb66d6282dd`  
		Last Modified: Thu, 23 Jan 2020 16:53:07 GMT  
		Size: 2.6 MB (2573620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe38d0bfb4cf690c35f5cad20f2b3852cf3e3feae187d049660d61066d34266`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7b0be037aec2a267ac29fa65d5d2944abe8469008d0642de65630db833c613`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 15.1 KB (15133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721302a401eba2bc95563c39d70c6ceb2622f40852963b48a63b9436ac729b35`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 1.5 MB (1462308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a3a38346255281bbb2fe4efbc071d94d6322906bce537bbfb2c901d054f30d`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3309d80a3f4f5007acb79f3c9791f4d35a740e7d64bc8a859f0781987c9e51`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
