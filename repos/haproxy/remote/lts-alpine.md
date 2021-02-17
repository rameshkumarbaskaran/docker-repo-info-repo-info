## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:6c7259a2c2f349a36f5b93a28e0fcf8a98473208e09ed19061a3b48045c9358b
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

### `haproxy:lts-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:ca20421f3092f180444fd2447179bcab52956c304bd5305629afd01af7e9ce66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9172399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd032c94c888c06064fd0ae28f7b4d55889830c7cc18b9af3aeb48979c8002c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Thu, 04 Feb 2021 00:27:11 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Feb 2021 21:25:32 GMT
ENV HAPROXY_VERSION=2.2.9
# Mon, 08 Feb 2021 21:25:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.9.tar.gz
# Mon, 08 Feb 2021 21:25:32 GMT
ENV HAPROXY_SHA256=21680459b08b9ba21c8cc9f5dbd0ee6e1842f57a3a67f87179871e1c13ebd4e3
# Mon, 08 Feb 2021 21:26:35 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Feb 2021 21:26:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Feb 2021 21:26:36 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Feb 2021 21:26:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Feb 2021 21:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Feb 2021 21:26:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9e1e30f5795f022d0e4f9637d193f599ec790bddf10d6a4dd0c027ebe33c75`  
		Last Modified: Thu, 04 Feb 2021 00:35:26 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665550e5feed50a6049a75c4107773911ca47f4f3d7aa90daf283e7721654081`  
		Last Modified: Mon, 08 Feb 2021 21:28:20 GMT  
		Size: 6.4 MB (6359325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d4efb1adba30cfc7723028f19937068bf6be8058d8a2e158a4d9f4b44e3abb`  
		Last Modified: Mon, 08 Feb 2021 21:28:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747fa427b44c399458f9a2aa01f5dfd95319ddf3048a6242546264acdd778169`  
		Last Modified: Mon, 08 Feb 2021 21:28:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:b3779467635a46474f1396db774326f38f5c59deaf1742f66f82908d44d132f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8865167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0a741212e3d187dc92c8b24eff55f73bb9a4124dedbdc6e18b493d778b7716`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:09:44 GMT
ENV HAPROXY_VERSION=2.2.9
# Wed, 17 Feb 2021 21:09:44 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.9.tar.gz
# Wed, 17 Feb 2021 21:09:45 GMT
ENV HAPROXY_SHA256=21680459b08b9ba21c8cc9f5dbd0ee6e1842f57a3a67f87179871e1c13ebd4e3
# Wed, 17 Feb 2021 21:10:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:10:10 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:10:10 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:10:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:10:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:10:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33ed1091d41f7d361940ea32a9681570c5519b8f7f3341df3391542752ba5e8`  
		Last Modified: Wed, 17 Feb 2021 21:12:52 GMT  
		Size: 6.2 MB (6241372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d0e02e84daf28f8384973a6485a947e6c0d67ebe88f62d7fb7ac3b8f2deb90`  
		Last Modified: Wed, 17 Feb 2021 21:12:50 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8438345f0d6da437248cb36334b9be83736143880b522c05acba835a97253c54`  
		Last Modified: Wed, 17 Feb 2021 21:12:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:41ff5a09c4fc5594c479c2da754caa70f8854f09fe40631b8c0f78a5d97fe8ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8583900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a67bfed0185c31e02fa442a2a584acb5104619ae936ac8d23956c9f6d9af94f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:51:18 GMT
ENV HAPROXY_VERSION=2.2.9
# Wed, 17 Feb 2021 21:51:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.9.tar.gz
# Wed, 17 Feb 2021 21:51:21 GMT
ENV HAPROXY_SHA256=21680459b08b9ba21c8cc9f5dbd0ee6e1842f57a3a67f87179871e1c13ebd4e3
# Wed, 17 Feb 2021 21:51:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:51:45 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:51:46 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:51:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:51:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570eb6e11fd2679d838ddc7143dddcaa905bf623bb0ae4d6bcdb623892cd6d19`  
		Last Modified: Wed, 17 Feb 2021 21:55:25 GMT  
		Size: 6.2 MB (6158251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5bb88e9c581968612cea57ee0f6a5cc54653041a30f166e70e7f3f0d3ab374`  
		Last Modified: Wed, 17 Feb 2021 21:55:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3240d680a0dbd7d984c83c329a9b50d44b41ff1b7b4bf67cfd22d651d97831b0`  
		Last Modified: Wed, 17 Feb 2021 21:55:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:38f2c4bb57e1ab45162bdb2769b5ae8ced4021dc110a099227fbc0db33875760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d85cc5cda84820104e634ae51f03dd9312d9b2ef864fa6150eff08727754c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:37:40 GMT
ENV HAPROXY_VERSION=2.2.9
# Wed, 17 Feb 2021 21:37:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.9.tar.gz
# Wed, 17 Feb 2021 21:37:42 GMT
ENV HAPROXY_SHA256=21680459b08b9ba21c8cc9f5dbd0ee6e1842f57a3a67f87179871e1c13ebd4e3
# Wed, 17 Feb 2021 21:38:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:38:05 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:38:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:38:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:38:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:38:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8875b7f3ff9cfbb8692349d47ce995a8f6ba5cde46f5615cde0fe1d0cda891b2`  
		Last Modified: Wed, 17 Feb 2021 21:41:40 GMT  
		Size: 6.4 MB (6366737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698c7b38c6ce90770fbeca8b200d103cc2e5a3ad90f7668115faf660dcb62af`  
		Last Modified: Wed, 17 Feb 2021 21:41:38 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f526d810c29e9d40168b915c940e92c60c76aaf721ab23a66da1e7c65e81b476`  
		Last Modified: Wed, 17 Feb 2021 21:41:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:e331beb6689dfcdfb6559ff0eeae9269ac7b763c258e79c5c929ad2ac6e2e9b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9008673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c048fd280de8b7af92baa4db1ac07cb6a3f1aea7494ec21fca2507187e44e85a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 28 Jan 2021 23:38:31 GMT
ADD file:c0e9ea135d66ad6504c77915a7a48b3bead60892d155d3258b746cb4945981c0 in / 
# Thu, 28 Jan 2021 23:38:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Feb 2021 00:47:32 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Feb 2021 20:48:00 GMT
ENV HAPROXY_VERSION=2.2.9
# Mon, 08 Feb 2021 20:48:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.9.tar.gz
# Mon, 08 Feb 2021 20:48:00 GMT
ENV HAPROXY_SHA256=21680459b08b9ba21c8cc9f5dbd0ee6e1842f57a3a67f87179871e1c13ebd4e3
# Mon, 08 Feb 2021 20:49:13 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Feb 2021 20:49:13 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Feb 2021 20:49:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Feb 2021 20:49:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Feb 2021 20:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Feb 2021 20:49:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3fea00a81341ce917db671eb3ad24ef5750cb6928b7f760e3ce4dab619eeb1fa`  
		Last Modified: Thu, 28 Jan 2021 23:39:02 GMT  
		Size: 2.8 MB (2817627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da9a2f27268a77730c5403499dd5715d18b02d22c2e8ba9c3bc58893667b493`  
		Last Modified: Thu, 04 Feb 2021 01:00:12 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafd284f48605f5e7fe795184ff92973ff1b70a1da23c28fcfafb3b481f2e7cb`  
		Last Modified: Mon, 08 Feb 2021 20:50:47 GMT  
		Size: 6.2 MB (6189291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fa580d0375094f3e860ea2df9bccc7f949827d3a581b096bfe4a9fe3f71d67`  
		Last Modified: Mon, 08 Feb 2021 20:50:46 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f15df774e704a404a3a9705fbec665f644b24b4c48939c6a2f4592a78033cae`  
		Last Modified: Mon, 08 Feb 2021 20:50:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:4c0834a4acffacf8777db2e272fb2624bac0aac4bc17ca5232bd5204996bb463
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9486526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad75dfc0deac8dc00e27e480905e6470f4ef0aa89b576cf75f86dcd0040fc69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 28 Jan 2021 23:55:50 GMT
ADD file:b14fd5f3f7fcd16e2b4ec6932d3e9c07c7400c577cee5fdcb88b0795a70a7bfb in / 
# Thu, 28 Jan 2021 23:55:52 GMT
CMD ["/bin/sh"]
# Thu, 04 Feb 2021 00:43:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Feb 2021 21:42:53 GMT
ENV HAPROXY_VERSION=2.2.9
# Mon, 08 Feb 2021 21:42:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.9.tar.gz
# Mon, 08 Feb 2021 21:43:01 GMT
ENV HAPROXY_SHA256=21680459b08b9ba21c8cc9f5dbd0ee6e1842f57a3a67f87179871e1c13ebd4e3
# Mon, 08 Feb 2021 21:43:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Feb 2021 21:43:56 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Feb 2021 21:43:59 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Feb 2021 21:44:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Feb 2021 21:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Feb 2021 21:44:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f3b94a1d8d591af02f1b419642bee91066ecbb9c65099d6903deed310fd1c2ff`  
		Last Modified: Thu, 28 Jan 2021 23:56:32 GMT  
		Size: 2.8 MB (2812517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0497dab5f8ffa38706eeb6cb666d8a80582b365f884d1eb1665114c9e761c28`  
		Last Modified: Thu, 04 Feb 2021 00:58:48 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb218635b97cdfb29d76a6ce0e36396199dcf0eb2b2338f2e5b302766c2360b`  
		Last Modified: Mon, 08 Feb 2021 21:46:30 GMT  
		Size: 6.7 MB (6672250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a4b142afeff254a3e125ea0911f863bff3f38f805f5066cdfdcd2b6e5fd012`  
		Last Modified: Mon, 08 Feb 2021 21:46:28 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f99c1cd88467139339191b1038aab10a6acbdb26f2a6e0b4decf597f3c776f4`  
		Last Modified: Mon, 08 Feb 2021 21:46:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:f02f73b15cc7346bec4479870617a470666b82ed716051eaade9e9cfb2081705
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8927086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94eadb596197a69344b7a501c64c29668e55eb488452715554f4feacdaf78de9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:36:53 GMT
ENV HAPROXY_VERSION=2.2.9
# Wed, 17 Feb 2021 21:36:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.9.tar.gz
# Wed, 17 Feb 2021 21:36:55 GMT
ENV HAPROXY_SHA256=21680459b08b9ba21c8cc9f5dbd0ee6e1842f57a3a67f87179871e1c13ebd4e3
# Wed, 17 Feb 2021 21:38:17 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:38:19 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:38:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:38:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:38:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:38:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807c57b31569b9f2cc34a0ab930fcccadd665ae92e19bec19435073b2f205a1e`  
		Last Modified: Wed, 17 Feb 2021 21:44:19 GMT  
		Size: 6.3 MB (6322948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a24c8dba098d25fbe8020ce100c5d8dc0c7e6ce16025fc4054d0cb0def20e26`  
		Last Modified: Wed, 17 Feb 2021 21:44:18 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fac4aae53b8792d803086946ef7b41800b2f91ccdf0d5f985346086598ab00`  
		Last Modified: Wed, 17 Feb 2021 21:44:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
