## `kong:latest`

```console
$ docker pull kong@sha256:803bda2f6c38fc042d3ac93625eec8acf1e4dec8db05566876187bb500555394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:7b259d28f8108b961de8001887d3bf1297f812a1456db19bca24e6eeb2c9b9cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51522512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712ffde79f4ab54edaaeb5188a3086e60f6bf4729459b724c58a651dae40ee9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:00:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 06 Oct 2022 23:00:54 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:00:54 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:00:54 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:00:54 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:00:54 GMT
ARG KONG_VERSION=3.0.0
# Thu, 06 Oct 2022 23:00:54 GMT
ENV KONG_VERSION=3.0.0
# Thu, 06 Oct 2022 23:00:54 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Thu, 06 Oct 2022 23:00:55 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Thu, 06 Oct 2022 23:01:03 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:04 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:04 GMT
USER kong
# Thu, 06 Oct 2022 23:01:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:04 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd92c70efef838622de7ec873d6e99abea86fe7547f5686b49707d02b5a7436b`  
		Last Modified: Thu, 06 Oct 2022 23:02:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46e65db14b2721c441faf7349324031c1da43116748d795b2537d1c5c02d46`  
		Last Modified: Thu, 06 Oct 2022 23:02:38 GMT  
		Size: 48.7 MB (48715447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0a423f8e78c38f414b2543801e0a6fc4c7a42b3b227d2a9266006b3bfa9399`  
		Last Modified: Thu, 06 Oct 2022 23:02:30 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:637b414b942280d7fca43b0d2ed9ff7d61fa572378c09be78418e6494d1ce91c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50640392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585672c38dc3394c806de0345fcd9beecc3ae6881b3bef19c56e7e88f2b2c375`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:55:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 26 Oct 2022 01:55:25 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:55:25 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:55:25 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:55:25 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:55:25 GMT
ARG KONG_VERSION=3.0.0
# Wed, 26 Oct 2022 01:55:25 GMT
ENV KONG_VERSION=3.0.0
# Wed, 26 Oct 2022 01:55:25 GMT
ARG KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10
# Wed, 26 Oct 2022 01:55:25 GMT
ARG KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
# Wed, 26 Oct 2022 01:55:33 GMT
# ARGS: KONG_AMD64_SHA=b8e21beb32f803fae0959694ce7b6cec796a4159757e61b9cc0d30bed9682d10 KONG_ARM64_SHA=4c5407c5ef2f0f29468e15ea4dc6a3f27011dbde3ce18170e4a4fd7e2bb2c03b
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:55:33 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:55:33 GMT
USER kong
# Wed, 26 Oct 2022 01:55:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:55:33 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:55:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:55:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:55:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb1fb82bc55ec7a036feb4d3b02c0b13181514e5d6830b118a9033e9fd83a6`  
		Last Modified: Wed, 26 Oct 2022 01:58:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18603c90f4a736910b1f40a0594612e7393607e212c8c87d158442f777c85a2a`  
		Last Modified: Wed, 26 Oct 2022 01:58:49 GMT  
		Size: 47.9 MB (47931719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c460c022742388d271a465f07222095ab992662528d74de39655cff71bf6200`  
		Last Modified: Wed, 26 Oct 2022 01:58:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
