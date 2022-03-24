## `kong:alpine`

```console
$ docker pull kong@sha256:ec7199734e3af2d21dfcf566352b4cdf5c939ffcdf9a1cd0ad4f3ec6aac914b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:e69c33d595dfad78d8d8ddcc642716590f67ff2e194bab8dfed1bbb4fe72645e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49111377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56eee7f71a90ff92ce52f5e718328ec05ab8216c0429e7e49e505ddb08165992`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:34:59 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 23 Mar 2022 17:34:59 GMT
ARG ASSET=ce
# Wed, 23 Mar 2022 17:34:59 GMT
ENV ASSET=ce
# Wed, 23 Mar 2022 17:34:59 GMT
ARG EE_PORTS
# Wed, 23 Mar 2022 17:34:59 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 23 Mar 2022 17:34:59 GMT
ARG KONG_VERSION=2.8.0
# Wed, 23 Mar 2022 17:34:59 GMT
ENV KONG_VERSION=2.8.0
# Wed, 23 Mar 2022 17:35:00 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Wed, 23 Mar 2022 17:35:00 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Wed, 23 Mar 2022 17:35:07 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 23 Mar 2022 17:35:08 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 23 Mar 2022 17:35:08 GMT
USER kong
# Wed, 23 Mar 2022 17:35:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Mar 2022 17:35:08 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 23 Mar 2022 17:35:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Mar 2022 17:35:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 23 Mar 2022 17:35:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e314796d82ba8bbdea3761546e56faf95cc9145172d5447256b0271049c86f71`  
		Last Modified: Wed, 23 Mar 2022 17:35:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d9998634aab847b66646df4c2332f2eedf90870911d564e9473f32b20ec856`  
		Last Modified: Wed, 23 Mar 2022 17:36:05 GMT  
		Size: 46.3 MB (46297680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3148e2b67633bbfc03bad1f5bcd37d625b653b9ef9bca08ea5fca1ea87b1b1e`  
		Last Modified: Wed, 23 Mar 2022 17:35:58 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3d627216a6d1762692cffc71c1f8555cdd8e3c3ed122b2ef2d8b967ae6321e95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48304049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45462eb0d325b4c1b62d50d4de5c832990825a1625697ac36e657f9bcef8baf4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 06:06:58 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 24 Mar 2022 06:06:59 GMT
ARG ASSET=ce
# Thu, 24 Mar 2022 06:07:00 GMT
ENV ASSET=ce
# Thu, 24 Mar 2022 06:07:01 GMT
ARG EE_PORTS
# Thu, 24 Mar 2022 06:07:03 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 24 Mar 2022 06:07:03 GMT
ARG KONG_VERSION=2.8.0
# Thu, 24 Mar 2022 06:07:04 GMT
ENV KONG_VERSION=2.8.0
# Thu, 24 Mar 2022 06:07:05 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Thu, 24 Mar 2022 06:07:06 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Thu, 24 Mar 2022 06:07:13 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 24 Mar 2022 06:07:14 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 24 Mar 2022 06:07:14 GMT
USER kong
# Thu, 24 Mar 2022 06:07:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Mar 2022 06:07:16 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 24 Mar 2022 06:07:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 24 Mar 2022 06:07:18 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 24 Mar 2022 06:07:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea41f92bdfaf6f5c6f7c588cc730ad0aea173f124a1ed6777f4312d2a6198d8`  
		Last Modified: Thu, 24 Mar 2022 06:14:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6905b618a271a67b1c740060ac377b99759e34b1201eea749da82e5543b1029c`  
		Last Modified: Thu, 24 Mar 2022 06:14:09 GMT  
		Size: 45.6 MB (45588319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80012ba1379e1af026c4b7541a4ee96040a5fdbcb2bd3b669e531ecb1827e3d`  
		Last Modified: Thu, 24 Mar 2022 06:14:00 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
