## `kong:latest`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:e7f75a2e891f86caf9a70483ad7cbde119d7594149517fafe619b27bee61d349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49125256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8301ad2c6ccefa9744c675de2e3776def471cb145084c87faa69b863bde93cd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:31:04 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:04 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:31:13 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:31:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:31:13 GMT
USER kong
# Tue, 12 Apr 2022 19:31:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:31:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:31:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:31:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:31:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389c4f1235973b918da1c03c0ab36b3fe30f024ed66d40c2704a5e0759137272`  
		Last Modified: Tue, 12 Apr 2022 19:34:09 GMT  
		Size: 46.3 MB (46309685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd99fa0f49fc3b1008ca9553bff84563001d150bed9eec2cc9df121d5db0927b`  
		Last Modified: Tue, 12 Apr 2022 19:34:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b5dd30242a9c70c3f3fe1f1eed665d3f1f3280dd167fe339ff8c991c93b1a129
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48318586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21617654cc9d61550449c01006c561ca0c6bb1f7212bb27a056dc85184de9341`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:57:42 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:43 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:44 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:57:45 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:57:54 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:57:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:57:55 GMT
USER kong
# Tue, 12 Apr 2022 19:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:57:57 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:57:58 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:57:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:58:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1ac9a25b76951006c1ab965d664048643344f28e6224df493b5ed8f25c2627`  
		Last Modified: Tue, 12 Apr 2022 20:11:06 GMT  
		Size: 45.6 MB (45601096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8881b423857a7b53f2a070f5501cfaf8f63792c1f400fc72ec6cb31aaf6b52f0`  
		Last Modified: Tue, 12 Apr 2022 20:10:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
