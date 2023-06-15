## `kong:alpine`

```console
$ docker pull kong@sha256:aae539892ee4f08d979274768504d5e592928b1d57a824e3436d627a8588fe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:0259087c5093b770b34ca17d3be227a9264e2c5658c58563c01283b12d7c49ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34222118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90459c3fc97f37b85cb1fa39db3539cc1cbaf0ac2c8d9b58ad9e033f95165008`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:24:27 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 06:24:27 GMT
ARG KONG_VERSION=3.3.0
# Thu, 15 Jun 2023 06:24:27 GMT
ENV KONG_VERSION=3.3.0
# Thu, 15 Jun 2023 06:24:27 GMT
ARG KONG_AMD64_SHA=494522d5ef9baf674272bbb7075e406a4515a7475253fd3026cc7ca9451612a2
# Thu, 15 Jun 2023 06:24:27 GMT
ARG KONG_PREFIX=/usr/local/kong
# Thu, 15 Jun 2023 06:24:27 GMT
ENV KONG_PREFIX=/usr/local/kong
# Thu, 15 Jun 2023 06:24:27 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 06:24:28 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:24:28 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 06:24:34 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=494522d5ef9baf674272bbb7075e406a4515a7475253fd3026cc7ca9451612a2
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     KONG_SHA256=$KONG_AMD64_SHA ;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 06:24:34 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:24:34 GMT
USER kong
# Thu, 15 Jun 2023 06:24:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:24:34 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:24:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:24:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:24:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bf8f4939b0d0d869272046c9d70b9159d8da43fcbe49aa3db948aeec25ccc4`  
		Last Modified: Thu, 15 Jun 2023 06:25:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72589f98cfb44bd3f9dca2c93d93173361a0ac30a8d5a5a11639bafaecba65e`  
		Last Modified: Thu, 15 Jun 2023 06:25:58 GMT  
		Size: 30.8 MB (30846114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd32791a2d9c85fcb9b2a8553438aa66214a402cd38b29453bbc9b72bf4f76e`  
		Last Modified: Thu, 15 Jun 2023 06:25:53 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
