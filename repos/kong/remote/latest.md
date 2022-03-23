## `kong:latest`

```console
$ docker pull kong@sha256:bcea8751356d0ca7fb8f5a28bed45f708b29be3a0965ba29d3dad418c23a80c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

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

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f4721fd5c54f232a27a78ad0f75a4b6939f746ea4c871e9dba488923aabc8e19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48304606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c857b43599f761099a0ceb2cfa5593d758d5f28243360f4ee4b90a7f0ecf01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:48:27 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 21:48:28 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 21:48:29 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 21:48:30 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 21:48:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 21:48:32 GMT
ARG KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 21:48:33 GMT
ENV KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 21:48:34 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Thu, 17 Mar 2022 21:48:35 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Thu, 17 Mar 2022 21:48:43 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:48:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:48:44 GMT
USER kong
# Thu, 17 Mar 2022 21:48:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:48:46 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:48:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:48:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:48:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcca8a3679eb011a753c11e924ab188577eb029867c2c9cc93f7e2de0dd42e1d`  
		Last Modified: Thu, 17 Mar 2022 21:57:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5354efff73660394c0f9ee520740504645bd387e8e9782f1630ea7a8e174e15`  
		Last Modified: Thu, 17 Mar 2022 21:57:10 GMT  
		Size: 45.6 MB (45588788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844cbd1bcb39efd214d04547dd56a6597ead9300709f1dae3e39d0815f2c0c5b`  
		Last Modified: Thu, 17 Mar 2022 21:57:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
