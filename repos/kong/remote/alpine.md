## `kong:alpine`

```console
$ docker pull kong@sha256:a0f19b375b5e6f35e1a46b9c5b5e65f53fe3258c8994bc9298a353d6f1789afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:95515d0f66dd958be1e30af772ada51bd4812d2a27bcb9124074fd1a2df4402e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49865802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51b92ff33146bb0aa7d22bd05cf622124574febe4ee673d92dfed8299b140ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:01 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:02 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:02 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:04 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:12 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:13 GMT
USER kong
# Sat, 13 Nov 2021 05:49:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b2c66462e7a485d21bf9baf11a6e252511cd3612b6fa68b0c1da6972f4cd`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c7e18e0a769d4001d507fbe88c18e222f1ef8b290b08b684cbe031f308a212`  
		Last Modified: Sat, 13 Nov 2021 05:50:51 GMT  
		Size: 47.0 MB (47041810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9e277edccd9c623819e5913361a38ef18b0d49d8563a765c7cbda0260b9d4`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:65530f037f12433ea809bae28fc24c1572737cda5126ef4745c6d32e349ac880
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49220211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4725fbe7d43e3205d4b59651b38492c470131a539294fbb5e69c6d91f44b89d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:11:28 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 06:11:29 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 06:11:30 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 06:11:31 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 06:11:33 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 17 Dec 2021 19:00:49 GMT
ARG KONG_VERSION=2.7.0
# Fri, 17 Dec 2021 19:00:50 GMT
ENV KONG_VERSION=2.7.0
# Fri, 17 Dec 2021 19:00:51 GMT
ARG KONG_AMD64_SHA=4caec31903319d1c09542e967e6e4d601bc469b5f28b13f83907a8115a9ff2e5
# Fri, 17 Dec 2021 19:00:52 GMT
ARG KONG_ARM64_SHA=923997ff72b52058f0c91ba09e400ea43c89f9d9e82ccb74f188a44e461a35b7
# Fri, 17 Dec 2021 19:01:19 GMT
# ARGS: KONG_AMD64_SHA=4caec31903319d1c09542e967e6e4d601bc469b5f28b13f83907a8115a9ff2e5 KONG_ARM64_SHA=923997ff72b52058f0c91ba09e400ea43c89f9d9e82ccb74f188a44e461a35b7
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 17 Dec 2021 19:01:20 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 17 Dec 2021 19:01:20 GMT
USER kong
# Fri, 17 Dec 2021 19:01:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 17 Dec 2021 19:01:22 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 17 Dec 2021 19:01:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Dec 2021 19:01:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 17 Dec 2021 19:01:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53315a86544ab6e48bbf724baae0beec28097187f7ffcda4174c31e3cbb0224e`  
		Last Modified: Sat, 13 Nov 2021 06:16:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73af152486c60eac70ed3dddb3b5f38dc02c78b8f47f4dd1b8b85a9c952099cc`  
		Last Modified: Fri, 17 Dec 2021 19:07:19 GMT  
		Size: 46.5 MB (46501501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539bcc814240d49734fbef7216ba4e444af56798b1de7719bde1aa66d7f9e38d`  
		Last Modified: Fri, 17 Dec 2021 19:07:10 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
