<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.5`](#kong25)
-	[`kong:2.5-ubuntu`](#kong25-ubuntu)
-	[`kong:2.5.2`](#kong252)
-	[`kong:2.5.2-alpine`](#kong252-alpine)
-	[`kong:2.5.2-ubuntu`](#kong252-ubuntu)
-	[`kong:2.6`](#kong26)
-	[`kong:2.6-ubuntu`](#kong26-ubuntu)
-	[`kong:2.6.1`](#kong261)
-	[`kong:2.6.1-alpine`](#kong261-alpine)
-	[`kong:2.6.1-ubuntu`](#kong261-ubuntu)
-	[`kong:2.7`](#kong27)
-	[`kong:2.7-ubuntu`](#kong27-ubuntu)
-	[`kong:2.7.2`](#kong272)
-	[`kong:2.7.2-alpine`](#kong272-alpine)
-	[`kong:2.7.2-ubuntu`](#kong272-ubuntu)
-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.1`](#kong281)
-	[`kong:2.8.1-alpine`](#kong281-alpine)
-	[`kong:2.8.1-ubuntu`](#kong281-ubuntu)
-	[`kong:3.0`](#kong30)
-	[`kong:3.0-ubuntu`](#kong30-ubuntu)
-	[`kong:3.0.0`](#kong300)
-	[`kong:3.0.0-alpine`](#kong300-alpine)
-	[`kong:3.0.0-ubuntu`](#kong300-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.5`

```console
$ docker pull kong@sha256:646edcf649badc573fd7bb67011ae01d3c609ccd4857701f0b8f8fd57ac2c7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:05289c41fbd1aca217f6db0d25fbb2865b062e209743ac04119daea13015654f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49212370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b83ca7b49ebd6c41ab1dd1eff15083f2ce7cc7ce42ae1da19a4e13e02ee035`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:23 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:23 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:50 GMT
ARG KONG_VERSION=2.5.2
# Thu, 06 Oct 2022 23:01:50 GMT
ENV KONG_VERSION=2.5.2
# Thu, 06 Oct 2022 23:01:50 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Thu, 06 Oct 2022 23:01:50 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Thu, 06 Oct 2022 23:01:57 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:58 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:58 GMT
USER kong
# Thu, 06 Oct 2022 23:01:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:58 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:58 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:58 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712f9007996b849b4ca5751d9caac52946d8e35200fe77a0e58b376287bbbd`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669c28460b5bfedf1255235b6e1a6b33b6be4927235fd60cb1e16bd6a0ff29f9`  
		Last Modified: Thu, 06 Oct 2022 23:04:02 GMT  
		Size: 46.4 MB (46387849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b879cb95f5a94f57e19a2f23ee6511900441e380da40ee1c2ace9ded3136ee4f`  
		Last Modified: Thu, 06 Oct 2022 23:03:54 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:96db3d7827cde726cd58c008803d7d877bd1845094ca630a82bb022e9a389a58
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48404032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4b43a1cbf4ba5c84b40c35b8707aad4db9347f49e735d34efc94ff90a40d22`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:40 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:40 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:57:40 GMT
ARG KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:40 GMT
ENV KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:40 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Wed, 26 Oct 2022 01:57:40 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Wed, 26 Oct 2022 01:57:46 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:57:47 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:47 GMT
USER kong
# Wed, 26 Oct 2022 01:57:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:47 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:47 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02eeaaa55fc156cb548d037ac8e47ea838e55c008d6870c9ad0428e097097e9`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3df97541e884787e587d96697cbdd887c5b145767cdfe647b8776b85196422f`  
		Last Modified: Wed, 26 Oct 2022 02:01:29 GMT  
		Size: 45.7 MB (45684582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61696fbb2f2958b76ed59c959b51bac5e25564f21e4f5946d124fc6affdc0630`  
		Last Modified: Wed, 26 Oct 2022 02:01:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:4f1be3c3c51735bc38bf3f697ab02251714fb6ebce6edeb02655483756a454b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e632ff086a0398c2e689ad15179a4c1a21a52bf97eae02e9cbe9bcbc8bc41453
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121373747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bc344365a9680adcc5a9b5f47c0fa586d0277ce2dcf80b2c63ee0c015530c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 18:05:56 GMT
ENV KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Wed, 05 Oct 2022 18:06:17 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:06:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:06:18 GMT
USER kong
# Wed, 05 Oct 2022 18:06:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:06:19 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:06:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:06:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:06:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feafaa2914aeeed8aa4de482bc243e365ed0f4ed3e2fbae0768c8a361cb9754c`  
		Last Modified: Wed, 05 Oct 2022 18:08:48 GMT  
		Size: 67.7 MB (67716453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a07f475cc0994afcdbe19a018a9413c11861f5a8e22c3cb7d88a87b158083ef`  
		Last Modified: Wed, 05 Oct 2022 18:08:36 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c4d771265105107b80fdd0c59c2054d5837caf83d76b3bb11f9a0c0f19492bfa
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118346925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484481a63e074adeefd60c776b9316aeb130900b404e1c5d978ef687b4fd949f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:56:21 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:21 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:57:50 GMT
ARG KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:50 GMT
ENV KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:50 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Wed, 26 Oct 2022 01:57:50 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Wed, 26 Oct 2022 01:58:05 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:58:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:58:06 GMT
USER kong
# Wed, 26 Oct 2022 01:58:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:58:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:58:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:58:06 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:58:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f13f9d5d996e141886cffb3feec65b77fb24a51d5f42dc401d608fdec73f4c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2749d9ba1fa560c856c7e6fd0b63ec80a2c0a667b2ce32aa904361ab9b78133f`  
		Last Modified: Wed, 26 Oct 2022 02:01:50 GMT  
		Size: 66.1 MB (66068093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad99bf7b3aeecc65299a0b730bafc3ab80188e626f9f188758d95de65ba1eae`  
		Last Modified: Wed, 26 Oct 2022 02:01:41 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2`

```console
$ docker pull kong@sha256:646edcf649badc573fd7bb67011ae01d3c609ccd4857701f0b8f8fd57ac2c7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2` - linux; amd64

```console
$ docker pull kong@sha256:05289c41fbd1aca217f6db0d25fbb2865b062e209743ac04119daea13015654f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49212370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b83ca7b49ebd6c41ab1dd1eff15083f2ce7cc7ce42ae1da19a4e13e02ee035`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:23 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:23 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:50 GMT
ARG KONG_VERSION=2.5.2
# Thu, 06 Oct 2022 23:01:50 GMT
ENV KONG_VERSION=2.5.2
# Thu, 06 Oct 2022 23:01:50 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Thu, 06 Oct 2022 23:01:50 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Thu, 06 Oct 2022 23:01:57 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:58 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:58 GMT
USER kong
# Thu, 06 Oct 2022 23:01:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:58 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:58 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:58 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712f9007996b849b4ca5751d9caac52946d8e35200fe77a0e58b376287bbbd`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669c28460b5bfedf1255235b6e1a6b33b6be4927235fd60cb1e16bd6a0ff29f9`  
		Last Modified: Thu, 06 Oct 2022 23:04:02 GMT  
		Size: 46.4 MB (46387849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b879cb95f5a94f57e19a2f23ee6511900441e380da40ee1c2ace9ded3136ee4f`  
		Last Modified: Thu, 06 Oct 2022 23:03:54 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:96db3d7827cde726cd58c008803d7d877bd1845094ca630a82bb022e9a389a58
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48404032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4b43a1cbf4ba5c84b40c35b8707aad4db9347f49e735d34efc94ff90a40d22`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:40 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:40 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:57:40 GMT
ARG KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:40 GMT
ENV KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:40 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Wed, 26 Oct 2022 01:57:40 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Wed, 26 Oct 2022 01:57:46 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:57:47 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:47 GMT
USER kong
# Wed, 26 Oct 2022 01:57:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:47 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:47 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02eeaaa55fc156cb548d037ac8e47ea838e55c008d6870c9ad0428e097097e9`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3df97541e884787e587d96697cbdd887c5b145767cdfe647b8776b85196422f`  
		Last Modified: Wed, 26 Oct 2022 02:01:29 GMT  
		Size: 45.7 MB (45684582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61696fbb2f2958b76ed59c959b51bac5e25564f21e4f5946d124fc6affdc0630`  
		Last Modified: Wed, 26 Oct 2022 02:01:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-alpine`

```console
$ docker pull kong@sha256:646edcf649badc573fd7bb67011ae01d3c609ccd4857701f0b8f8fd57ac2c7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:05289c41fbd1aca217f6db0d25fbb2865b062e209743ac04119daea13015654f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49212370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b83ca7b49ebd6c41ab1dd1eff15083f2ce7cc7ce42ae1da19a4e13e02ee035`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:23 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:23 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:50 GMT
ARG KONG_VERSION=2.5.2
# Thu, 06 Oct 2022 23:01:50 GMT
ENV KONG_VERSION=2.5.2
# Thu, 06 Oct 2022 23:01:50 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Thu, 06 Oct 2022 23:01:50 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Thu, 06 Oct 2022 23:01:57 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:58 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:58 GMT
USER kong
# Thu, 06 Oct 2022 23:01:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:58 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:58 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:58 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712f9007996b849b4ca5751d9caac52946d8e35200fe77a0e58b376287bbbd`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669c28460b5bfedf1255235b6e1a6b33b6be4927235fd60cb1e16bd6a0ff29f9`  
		Last Modified: Thu, 06 Oct 2022 23:04:02 GMT  
		Size: 46.4 MB (46387849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b879cb95f5a94f57e19a2f23ee6511900441e380da40ee1c2ace9ded3136ee4f`  
		Last Modified: Thu, 06 Oct 2022 23:03:54 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:96db3d7827cde726cd58c008803d7d877bd1845094ca630a82bb022e9a389a58
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48404032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4b43a1cbf4ba5c84b40c35b8707aad4db9347f49e735d34efc94ff90a40d22`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:40 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:40 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:57:40 GMT
ARG KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:40 GMT
ENV KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:40 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Wed, 26 Oct 2022 01:57:40 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Wed, 26 Oct 2022 01:57:46 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:57:47 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:47 GMT
USER kong
# Wed, 26 Oct 2022 01:57:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:47 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:47 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02eeaaa55fc156cb548d037ac8e47ea838e55c008d6870c9ad0428e097097e9`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3df97541e884787e587d96697cbdd887c5b145767cdfe647b8776b85196422f`  
		Last Modified: Wed, 26 Oct 2022 02:01:29 GMT  
		Size: 45.7 MB (45684582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61696fbb2f2958b76ed59c959b51bac5e25564f21e4f5946d124fc6affdc0630`  
		Last Modified: Wed, 26 Oct 2022 02:01:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-ubuntu`

```console
$ docker pull kong@sha256:4f1be3c3c51735bc38bf3f697ab02251714fb6ebce6edeb02655483756a454b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e632ff086a0398c2e689ad15179a4c1a21a52bf97eae02e9cbe9bcbc8bc41453
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121373747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bc344365a9680adcc5a9b5f47c0fa586d0277ce2dcf80b2c63ee0c015530c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 18:05:56 GMT
ENV KONG_VERSION=2.5.2
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Wed, 05 Oct 2022 18:05:56 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Wed, 05 Oct 2022 18:06:17 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:06:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:06:18 GMT
USER kong
# Wed, 05 Oct 2022 18:06:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:06:19 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:06:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:06:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:06:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feafaa2914aeeed8aa4de482bc243e365ed0f4ed3e2fbae0768c8a361cb9754c`  
		Last Modified: Wed, 05 Oct 2022 18:08:48 GMT  
		Size: 67.7 MB (67716453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a07f475cc0994afcdbe19a018a9413c11861f5a8e22c3cb7d88a87b158083ef`  
		Last Modified: Wed, 05 Oct 2022 18:08:36 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c4d771265105107b80fdd0c59c2054d5837caf83d76b3bb11f9a0c0f19492bfa
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118346925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484481a63e074adeefd60c776b9316aeb130900b404e1c5d978ef687b4fd949f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:56:21 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:21 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:57:50 GMT
ARG KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:50 GMT
ENV KONG_VERSION=2.5.2
# Wed, 26 Oct 2022 01:57:50 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Wed, 26 Oct 2022 01:57:50 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Wed, 26 Oct 2022 01:58:05 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:58:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:58:06 GMT
USER kong
# Wed, 26 Oct 2022 01:58:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:58:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:58:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:58:06 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:58:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f13f9d5d996e141886cffb3feec65b77fb24a51d5f42dc401d608fdec73f4c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2749d9ba1fa560c856c7e6fd0b63ec80a2c0a667b2ce32aa904361ab9b78133f`  
		Last Modified: Wed, 26 Oct 2022 02:01:50 GMT  
		Size: 66.1 MB (66068093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad99bf7b3aeecc65299a0b730bafc3ab80188e626f9f188758d95de65ba1eae`  
		Last Modified: Wed, 26 Oct 2022 02:01:41 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:80e9b3d71e1b4c969368c10eb91d982d90ba4d6b880cf98b1a31cdea7c635b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

```console
$ docker pull kong@sha256:8b976b5e1f07a06c0d337ac2548b48147b0180b92e3b4aad8de6f47b02177f1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50233005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dda4b3d1de7ee2ca6ebe5ec1f2c84f6784f10ee8c8f10f0525738aa67b191d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:23 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:23 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:37 GMT
ARG KONG_VERSION=2.6.1
# Thu, 06 Oct 2022 23:01:37 GMT
ENV KONG_VERSION=2.6.1
# Thu, 06 Oct 2022 23:01:37 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Thu, 06 Oct 2022 23:01:37 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Thu, 06 Oct 2022 23:01:44 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:44 GMT
USER kong
# Thu, 06 Oct 2022 23:01:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:45 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712f9007996b849b4ca5751d9caac52946d8e35200fe77a0e58b376287bbbd`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfba4240422e95f3476c90d92e9255cfa6695fb3af89710a50538a16141d797`  
		Last Modified: Thu, 06 Oct 2022 23:03:42 GMT  
		Size: 47.4 MB (47408484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417a3349224dae27cda5dddd34c1f1da6015d5eaa81560431b42c522e6fbb0f`  
		Last Modified: Thu, 06 Oct 2022 23:03:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:877a5bbbdd99b3431b40910a75f1d9e5ab383705db19c8d440a66d392621b2cb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49638258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c66f77c91cea9e07d70c3610c298a4960e5d48949dd3ceab8e68fcf8073fd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:40 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:40 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:57:11 GMT
ARG KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:11 GMT
ENV KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:11 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Wed, 26 Oct 2022 01:57:11 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Wed, 26 Oct 2022 01:57:18 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:57:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:18 GMT
USER kong
# Wed, 26 Oct 2022 01:57:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:18 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02eeaaa55fc156cb548d037ac8e47ea838e55c008d6870c9ad0428e097097e9`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4390b7e58a4e526ba1db9214b8df2a7096a97ff67311e5aeb74a18510326d9`  
		Last Modified: Wed, 26 Oct 2022 02:00:52 GMT  
		Size: 46.9 MB (46918809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5011023c7752c06ab78770f9a7b400361036dd4010a9877f3db0d995bf61e954`  
		Last Modified: Wed, 26 Oct 2022 02:00:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:871ab3a9edd7346d77d87cd500884073c5572a220309231474f68d194bee6fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:62f0eb7ee8aecf4d9ae88517c0b54e9401f2a992719e7f38d592650d443e4370
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128258108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8466c81f7e147ef5ef114b87cf3a53fe0bf59eaa7df8336d594fadf88cf56e83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 18:05:26 GMT
ENV KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Wed, 05 Oct 2022 18:05:48 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:05:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:05:49 GMT
USER kong
# Wed, 05 Oct 2022 18:05:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:05:49 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:05:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:05:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:05:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e993696815ce3a452cb95ab776e9c62ff68517f43710256e73e840cffb96e`  
		Last Modified: Wed, 05 Oct 2022 18:08:25 GMT  
		Size: 74.6 MB (74600814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb74a132762f4f4e3c5e5039de49d10ffd3c81369242eb4030c36ad9517bfa`  
		Last Modified: Wed, 05 Oct 2022 18:08:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9fa6e474d79c26b0925cf3e341544379685ba7317c64a514e5bb6b8215f46a00
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125236371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f12596fd5f4f193d4f50592e765473581ffd5bc82e5831d6b7b1833d31df648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:56:21 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:21 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:57:21 GMT
ARG KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:21 GMT
ENV KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:21 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Wed, 26 Oct 2022 01:57:21 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Wed, 26 Oct 2022 01:57:37 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:57:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:38 GMT
USER kong
# Wed, 26 Oct 2022 01:57:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:38 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f13f9d5d996e141886cffb3feec65b77fb24a51d5f42dc401d608fdec73f4c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db40ebc071ab72c9a9c20f0f80ee32933c3764493827c173590563f31c0d7771`  
		Last Modified: Wed, 26 Oct 2022 02:01:13 GMT  
		Size: 73.0 MB (72957539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18adf6b3f887fbc4787108014ba58ab89c651de4d77dfd04b8516114fa21b37`  
		Last Modified: Wed, 26 Oct 2022 02:01:03 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1`

```console
$ docker pull kong@sha256:80e9b3d71e1b4c969368c10eb91d982d90ba4d6b880cf98b1a31cdea7c635b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1` - linux; amd64

```console
$ docker pull kong@sha256:8b976b5e1f07a06c0d337ac2548b48147b0180b92e3b4aad8de6f47b02177f1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50233005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dda4b3d1de7ee2ca6ebe5ec1f2c84f6784f10ee8c8f10f0525738aa67b191d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:23 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:23 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:37 GMT
ARG KONG_VERSION=2.6.1
# Thu, 06 Oct 2022 23:01:37 GMT
ENV KONG_VERSION=2.6.1
# Thu, 06 Oct 2022 23:01:37 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Thu, 06 Oct 2022 23:01:37 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Thu, 06 Oct 2022 23:01:44 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:44 GMT
USER kong
# Thu, 06 Oct 2022 23:01:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:45 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712f9007996b849b4ca5751d9caac52946d8e35200fe77a0e58b376287bbbd`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfba4240422e95f3476c90d92e9255cfa6695fb3af89710a50538a16141d797`  
		Last Modified: Thu, 06 Oct 2022 23:03:42 GMT  
		Size: 47.4 MB (47408484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417a3349224dae27cda5dddd34c1f1da6015d5eaa81560431b42c522e6fbb0f`  
		Last Modified: Thu, 06 Oct 2022 23:03:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:877a5bbbdd99b3431b40910a75f1d9e5ab383705db19c8d440a66d392621b2cb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49638258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c66f77c91cea9e07d70c3610c298a4960e5d48949dd3ceab8e68fcf8073fd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:40 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:40 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:57:11 GMT
ARG KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:11 GMT
ENV KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:11 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Wed, 26 Oct 2022 01:57:11 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Wed, 26 Oct 2022 01:57:18 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:57:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:18 GMT
USER kong
# Wed, 26 Oct 2022 01:57:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:18 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02eeaaa55fc156cb548d037ac8e47ea838e55c008d6870c9ad0428e097097e9`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4390b7e58a4e526ba1db9214b8df2a7096a97ff67311e5aeb74a18510326d9`  
		Last Modified: Wed, 26 Oct 2022 02:00:52 GMT  
		Size: 46.9 MB (46918809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5011023c7752c06ab78770f9a7b400361036dd4010a9877f3db0d995bf61e954`  
		Last Modified: Wed, 26 Oct 2022 02:00:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-alpine`

```console
$ docker pull kong@sha256:80e9b3d71e1b4c969368c10eb91d982d90ba4d6b880cf98b1a31cdea7c635b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:8b976b5e1f07a06c0d337ac2548b48147b0180b92e3b4aad8de6f47b02177f1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50233005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dda4b3d1de7ee2ca6ebe5ec1f2c84f6784f10ee8c8f10f0525738aa67b191d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:23 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:23 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:37 GMT
ARG KONG_VERSION=2.6.1
# Thu, 06 Oct 2022 23:01:37 GMT
ENV KONG_VERSION=2.6.1
# Thu, 06 Oct 2022 23:01:37 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Thu, 06 Oct 2022 23:01:37 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Thu, 06 Oct 2022 23:01:44 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:44 GMT
USER kong
# Thu, 06 Oct 2022 23:01:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:45 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712f9007996b849b4ca5751d9caac52946d8e35200fe77a0e58b376287bbbd`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfba4240422e95f3476c90d92e9255cfa6695fb3af89710a50538a16141d797`  
		Last Modified: Thu, 06 Oct 2022 23:03:42 GMT  
		Size: 47.4 MB (47408484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417a3349224dae27cda5dddd34c1f1da6015d5eaa81560431b42c522e6fbb0f`  
		Last Modified: Thu, 06 Oct 2022 23:03:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:877a5bbbdd99b3431b40910a75f1d9e5ab383705db19c8d440a66d392621b2cb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49638258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c66f77c91cea9e07d70c3610c298a4960e5d48949dd3ceab8e68fcf8073fd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:40 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:40 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:57:11 GMT
ARG KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:11 GMT
ENV KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:11 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Wed, 26 Oct 2022 01:57:11 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Wed, 26 Oct 2022 01:57:18 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:57:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:18 GMT
USER kong
# Wed, 26 Oct 2022 01:57:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:18 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02eeaaa55fc156cb548d037ac8e47ea838e55c008d6870c9ad0428e097097e9`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4390b7e58a4e526ba1db9214b8df2a7096a97ff67311e5aeb74a18510326d9`  
		Last Modified: Wed, 26 Oct 2022 02:00:52 GMT  
		Size: 46.9 MB (46918809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5011023c7752c06ab78770f9a7b400361036dd4010a9877f3db0d995bf61e954`  
		Last Modified: Wed, 26 Oct 2022 02:00:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-ubuntu`

```console
$ docker pull kong@sha256:871ab3a9edd7346d77d87cd500884073c5572a220309231474f68d194bee6fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:62f0eb7ee8aecf4d9ae88517c0b54e9401f2a992719e7f38d592650d443e4370
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128258108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8466c81f7e147ef5ef114b87cf3a53fe0bf59eaa7df8336d594fadf88cf56e83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 18:05:26 GMT
ENV KONG_VERSION=2.6.1
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Wed, 05 Oct 2022 18:05:26 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Wed, 05 Oct 2022 18:05:48 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:05:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:05:49 GMT
USER kong
# Wed, 05 Oct 2022 18:05:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:05:49 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:05:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:05:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:05:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e993696815ce3a452cb95ab776e9c62ff68517f43710256e73e840cffb96e`  
		Last Modified: Wed, 05 Oct 2022 18:08:25 GMT  
		Size: 74.6 MB (74600814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb74a132762f4f4e3c5e5039de49d10ffd3c81369242eb4030c36ad9517bfa`  
		Last Modified: Wed, 05 Oct 2022 18:08:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9fa6e474d79c26b0925cf3e341544379685ba7317c64a514e5bb6b8215f46a00
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125236371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f12596fd5f4f193d4f50592e765473581ffd5bc82e5831d6b7b1833d31df648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:56:21 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:21 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:57:21 GMT
ARG KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:21 GMT
ENV KONG_VERSION=2.6.1
# Wed, 26 Oct 2022 01:57:21 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Wed, 26 Oct 2022 01:57:21 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Wed, 26 Oct 2022 01:57:37 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:57:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:38 GMT
USER kong
# Wed, 26 Oct 2022 01:57:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:38 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f13f9d5d996e141886cffb3feec65b77fb24a51d5f42dc401d608fdec73f4c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db40ebc071ab72c9a9c20f0f80ee32933c3764493827c173590563f31c0d7771`  
		Last Modified: Wed, 26 Oct 2022 02:01:13 GMT  
		Size: 73.0 MB (72957539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18adf6b3f887fbc4787108014ba58ab89c651de4d77dfd04b8516114fa21b37`  
		Last Modified: Wed, 26 Oct 2022 02:01:03 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7`

```console
$ docker pull kong@sha256:fa2b440ddbc7b1836cf06c8380859d10889e4e1710a9e102851a993771450753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7` - linux; amd64

```console
$ docker pull kong@sha256:8d092fb34ec241f32d28a847c523d8343acc6fd124d9c741a345af7006b7f6df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50140063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7c0c4fabfb88b737b0346cad01366cd42c2ef0c01af6933b23bcc68f275eeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:23 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:23 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:24 GMT
ARG KONG_VERSION=2.7.2
# Thu, 06 Oct 2022 23:01:24 GMT
ENV KONG_VERSION=2.7.2
# Thu, 06 Oct 2022 23:01:24 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Thu, 06 Oct 2022 23:01:24 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Thu, 06 Oct 2022 23:01:31 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:31 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:31 GMT
USER kong
# Thu, 06 Oct 2022 23:01:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:32 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712f9007996b849b4ca5751d9caac52946d8e35200fe77a0e58b376287bbbd`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acde767c288c65146a32b71e68d2c25ff1803ac881577a77f6bfc3bdc82630e5`  
		Last Modified: Thu, 06 Oct 2022 23:03:22 GMT  
		Size: 47.3 MB (47315542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e54051d48e8ce97f13a7d5496d56b730a129bd4a03e80cc4eabb0f39010d55a`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:51fb88f395109af7ac336c5e4acb81ad3f91bcee3b09126f1833d64a72e2855c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2b826e36153cb909900fd41462eaa5242d25e7391a1e8c7631e8b08ba3346e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:40 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:40 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:56:40 GMT
ARG KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:41 GMT
ENV KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:41 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Wed, 26 Oct 2022 01:56:41 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Wed, 26 Oct 2022 01:56:47 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:56:48 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:48 GMT
USER kong
# Wed, 26 Oct 2022 01:56:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:48 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02eeaaa55fc156cb548d037ac8e47ea838e55c008d6870c9ad0428e097097e9`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286fb448394626b813089a35ce68138aebab777814749aa49139a4bddafb76dd`  
		Last Modified: Wed, 26 Oct 2022 02:00:14 GMT  
		Size: 46.8 MB (46837874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46cc6a3e5e78dc18516c26e6858e89f0ac10a6ba5b7e94e5db1c8d82906e7ae`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7-ubuntu`

```console
$ docker pull kong@sha256:8108520f19ada85e1f832d07109b6025b1dfb6cf4615e9f7d5affb6574ae38af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1b3b987b13fc81da2bc6d633049a829a93edc97c864045ef7face0cf839ef55b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128168397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71cac7eed8a53d0cc9fbe23a14c1512174123d29c4c74b29476d5576424a20e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 18:04:56 GMT
ENV KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Wed, 05 Oct 2022 18:05:18 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:05:19 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:05:19 GMT
USER kong
# Wed, 05 Oct 2022 18:05:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:05:19 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:05:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:05:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:05:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073853ff82a5607beb1a0cc44c91ba59a4d1122dcb52322cc1a5531bd62a43a2`  
		Last Modified: Wed, 05 Oct 2022 18:07:57 GMT  
		Size: 74.5 MB (74511102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2450b04737255f8e696efca60087f8daa06ac4202cd42d03d8fb4990a420f22`  
		Last Modified: Wed, 05 Oct 2022 18:07:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:38c4331af51cdf7d32de61c30e6850e1e17ade6e544703279064b99c0cf15cd7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125147723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea24d22be45d5e30ec9f25aa9d6aa7cbbb2361a38679e4d3a6ae628217b3e639`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:56:21 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:21 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:56:51 GMT
ARG KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:51 GMT
ENV KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:52 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Wed, 26 Oct 2022 01:56:52 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Wed, 26 Oct 2022 01:57:07 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:57:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:09 GMT
USER kong
# Wed, 26 Oct 2022 01:57:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:09 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f13f9d5d996e141886cffb3feec65b77fb24a51d5f42dc401d608fdec73f4c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75187d3ab169827a7e01a58e228cfebf8d432384abe7786ccf7d63dab3ce094`  
		Last Modified: Wed, 26 Oct 2022 02:00:35 GMT  
		Size: 72.9 MB (72868890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f66589105c4b27f983dec1fa16c8c270c50550a4cecb0e628f2bdc684fa0c01`  
		Last Modified: Wed, 26 Oct 2022 02:00:26 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2`

```console
$ docker pull kong@sha256:fa2b440ddbc7b1836cf06c8380859d10889e4e1710a9e102851a993771450753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2` - linux; amd64

```console
$ docker pull kong@sha256:8d092fb34ec241f32d28a847c523d8343acc6fd124d9c741a345af7006b7f6df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50140063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7c0c4fabfb88b737b0346cad01366cd42c2ef0c01af6933b23bcc68f275eeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:23 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:23 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:24 GMT
ARG KONG_VERSION=2.7.2
# Thu, 06 Oct 2022 23:01:24 GMT
ENV KONG_VERSION=2.7.2
# Thu, 06 Oct 2022 23:01:24 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Thu, 06 Oct 2022 23:01:24 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Thu, 06 Oct 2022 23:01:31 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:31 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:31 GMT
USER kong
# Thu, 06 Oct 2022 23:01:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:32 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712f9007996b849b4ca5751d9caac52946d8e35200fe77a0e58b376287bbbd`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acde767c288c65146a32b71e68d2c25ff1803ac881577a77f6bfc3bdc82630e5`  
		Last Modified: Thu, 06 Oct 2022 23:03:22 GMT  
		Size: 47.3 MB (47315542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e54051d48e8ce97f13a7d5496d56b730a129bd4a03e80cc4eabb0f39010d55a`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:51fb88f395109af7ac336c5e4acb81ad3f91bcee3b09126f1833d64a72e2855c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2b826e36153cb909900fd41462eaa5242d25e7391a1e8c7631e8b08ba3346e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:40 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:40 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:56:40 GMT
ARG KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:41 GMT
ENV KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:41 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Wed, 26 Oct 2022 01:56:41 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Wed, 26 Oct 2022 01:56:47 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:56:48 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:48 GMT
USER kong
# Wed, 26 Oct 2022 01:56:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:48 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02eeaaa55fc156cb548d037ac8e47ea838e55c008d6870c9ad0428e097097e9`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286fb448394626b813089a35ce68138aebab777814749aa49139a4bddafb76dd`  
		Last Modified: Wed, 26 Oct 2022 02:00:14 GMT  
		Size: 46.8 MB (46837874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46cc6a3e5e78dc18516c26e6858e89f0ac10a6ba5b7e94e5db1c8d82906e7ae`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-alpine`

```console
$ docker pull kong@sha256:fa2b440ddbc7b1836cf06c8380859d10889e4e1710a9e102851a993771450753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:8d092fb34ec241f32d28a847c523d8343acc6fd124d9c741a345af7006b7f6df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50140063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7c0c4fabfb88b737b0346cad01366cd42c2ef0c01af6933b23bcc68f275eeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:23 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:23 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:23 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:24 GMT
ARG KONG_VERSION=2.7.2
# Thu, 06 Oct 2022 23:01:24 GMT
ENV KONG_VERSION=2.7.2
# Thu, 06 Oct 2022 23:01:24 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Thu, 06 Oct 2022 23:01:24 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Thu, 06 Oct 2022 23:01:31 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:31 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:31 GMT
USER kong
# Thu, 06 Oct 2022 23:01:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:32 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712f9007996b849b4ca5751d9caac52946d8e35200fe77a0e58b376287bbbd`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acde767c288c65146a32b71e68d2c25ff1803ac881577a77f6bfc3bdc82630e5`  
		Last Modified: Thu, 06 Oct 2022 23:03:22 GMT  
		Size: 47.3 MB (47315542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e54051d48e8ce97f13a7d5496d56b730a129bd4a03e80cc4eabb0f39010d55a`  
		Last Modified: Thu, 06 Oct 2022 23:03:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:51fb88f395109af7ac336c5e4acb81ad3f91bcee3b09126f1833d64a72e2855c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2b826e36153cb909900fd41462eaa5242d25e7391a1e8c7631e8b08ba3346e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:40 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:40 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:40 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:40 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:56:40 GMT
ARG KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:41 GMT
ENV KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:41 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Wed, 26 Oct 2022 01:56:41 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Wed, 26 Oct 2022 01:56:47 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:56:48 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:48 GMT
USER kong
# Wed, 26 Oct 2022 01:56:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:48 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02eeaaa55fc156cb548d037ac8e47ea838e55c008d6870c9ad0428e097097e9`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286fb448394626b813089a35ce68138aebab777814749aa49139a4bddafb76dd`  
		Last Modified: Wed, 26 Oct 2022 02:00:14 GMT  
		Size: 46.8 MB (46837874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46cc6a3e5e78dc18516c26e6858e89f0ac10a6ba5b7e94e5db1c8d82906e7ae`  
		Last Modified: Wed, 26 Oct 2022 02:00:07 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-ubuntu`

```console
$ docker pull kong@sha256:8108520f19ada85e1f832d07109b6025b1dfb6cf4615e9f7d5affb6574ae38af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1b3b987b13fc81da2bc6d633049a829a93edc97c864045ef7face0cf839ef55b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128168397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71cac7eed8a53d0cc9fbe23a14c1512174123d29c4c74b29476d5576424a20e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 18:04:56 GMT
ENV KONG_VERSION=2.7.2
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Wed, 05 Oct 2022 18:04:56 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Wed, 05 Oct 2022 18:05:18 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:05:19 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:05:19 GMT
USER kong
# Wed, 05 Oct 2022 18:05:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:05:19 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:05:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:05:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:05:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073853ff82a5607beb1a0cc44c91ba59a4d1122dcb52322cc1a5531bd62a43a2`  
		Last Modified: Wed, 05 Oct 2022 18:07:57 GMT  
		Size: 74.5 MB (74511102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2450b04737255f8e696efca60087f8daa06ac4202cd42d03d8fb4990a420f22`  
		Last Modified: Wed, 05 Oct 2022 18:07:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:38c4331af51cdf7d32de61c30e6850e1e17ade6e544703279064b99c0cf15cd7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125147723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea24d22be45d5e30ec9f25aa9d6aa7cbbb2361a38679e4d3a6ae628217b3e639`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:56:21 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:21 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:56:51 GMT
ARG KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:51 GMT
ENV KONG_VERSION=2.7.2
# Wed, 26 Oct 2022 01:56:52 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Wed, 26 Oct 2022 01:56:52 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Wed, 26 Oct 2022 01:57:07 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:57:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:57:09 GMT
USER kong
# Wed, 26 Oct 2022 01:57:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:57:09 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:57:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:57:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:57:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f13f9d5d996e141886cffb3feec65b77fb24a51d5f42dc401d608fdec73f4c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75187d3ab169827a7e01a58e228cfebf8d432384abe7786ccf7d63dab3ce094`  
		Last Modified: Wed, 26 Oct 2022 02:00:35 GMT  
		Size: 72.9 MB (72868890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f66589105c4b27f983dec1fa16c8c270c50550a4cecb0e628f2bdc684fa0c01`  
		Last Modified: Wed, 26 Oct 2022 02:00:26 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8`

```console
$ docker pull kong@sha256:1b53405d8680a09d6f44494b7990bf7da2ea43f84a258c59717d4539abf09f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:e21b0b793879ab96720ed4188f9441260273f4bf775bcbff8d435e019ffb759a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49335657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cefb958bcd694597b65adc00053a762b1f9a6df3c6031af528d052d75a64e1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:10 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:10 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:10 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:10 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:10 GMT
ARG KONG_VERSION=2.8.1
# Thu, 06 Oct 2022 23:01:10 GMT
ENV KONG_VERSION=2.8.1
# Thu, 06 Oct 2022 23:01:10 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Thu, 06 Oct 2022 23:01:10 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Thu, 06 Oct 2022 23:01:17 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:18 GMT
USER kong
# Thu, 06 Oct 2022 23:01:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:18 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:18 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70653f7a2d526d9024e271d864947f47000d34d971f36a44665b51e8c3b739c`  
		Last Modified: Thu, 06 Oct 2022 23:02:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531e3bd93090d08ef911bb2c8320f2fef2428ef96597535a55111fda18efde52`  
		Last Modified: Thu, 06 Oct 2022 23:03:02 GMT  
		Size: 46.5 MB (46528590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814dd06d26c72ec884803b7dd47e90f8855d4df9267025e9eb33d22aaa061e88`  
		Last Modified: Thu, 06 Oct 2022 23:02:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8a5a7357d6cbda1840574130d109fc37b8088750d32c87b50f3b7909b7975425
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48524280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5957d67fc55af3d11bdbd87de76f7480e3c4d8bcb715d6cfd01922780f46ea9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:09 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:09 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:10 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:10 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:56:10 GMT
ARG KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:10 GMT
ENV KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:10 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Wed, 26 Oct 2022 01:56:10 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Wed, 26 Oct 2022 01:56:16 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:56:17 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:17 GMT
USER kong
# Wed, 26 Oct 2022 01:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:17 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd91e9229603b76d74826c966b221aacc86c840445a63234a9e2850a10a0062`  
		Last Modified: Wed, 26 Oct 2022 01:59:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450997ae687cb58c194a458badbbb0c90dc4aed7eab5e3b1db610305ef840dd0`  
		Last Modified: Wed, 26 Oct 2022 01:59:35 GMT  
		Size: 45.8 MB (45815605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8380bfcbd9b9294f70da613229b53465eef3ac9234edb9cbfb19006dbb36293`  
		Last Modified: Wed, 26 Oct 2022 01:59:28 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:9f9dddc7616066f7b02b0e1735133523502a96832f8ffcf4e83c348e99025fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:cedff6e436f88215dadcd6bf2d25062b9b5d3170ff6c9947b02c1319876e5fdb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121292578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142c60b0bbecd85bac643266c0995c1b42083af9b5c4da4d1ba31592bb7c7f8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 18:04:27 GMT
ENV KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Wed, 05 Oct 2022 18:04:48 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:04:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:04:49 GMT
USER kong
# Wed, 05 Oct 2022 18:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:04:50 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:04:50 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:04:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:04:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc176a053adb32647c56614ff026d0deba20cb6efd6372197e024bf7c5693e`  
		Last Modified: Wed, 05 Oct 2022 18:07:33 GMT  
		Size: 67.6 MB (67635284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69d17ca86369a39c8f6a302ebfa154002b3b253738effeb247bfa53ec0330cb`  
		Last Modified: Wed, 05 Oct 2022 18:07:21 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b3821340749f078fca49fdcf6c59874924c3bc99affad7eb4870a4c105283bd8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121736114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cd5e3353682a08855cc43120d77ffacbaba519aaf68736d4bed76ab5609ea4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:56:21 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:21 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:56:21 GMT
ARG KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:21 GMT
ENV KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:21 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Wed, 26 Oct 2022 01:56:21 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Wed, 26 Oct 2022 01:56:36 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:56:37 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:38 GMT
USER kong
# Wed, 26 Oct 2022 01:56:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:38 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f13f9d5d996e141886cffb3feec65b77fb24a51d5f42dc401d608fdec73f4c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955e7d3f453f82dabe911edc9a1755176cbb03bb5422778efe0345f2afb442a2`  
		Last Modified: Wed, 26 Oct 2022 01:59:56 GMT  
		Size: 69.5 MB (69457280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae91fafd7b2bd72f523a509de3e8ae8fe69535d0bab2a8bdbd09fb0ab63dd97a`  
		Last Modified: Wed, 26 Oct 2022 01:59:47 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1`

```console
$ docker pull kong@sha256:1b53405d8680a09d6f44494b7990bf7da2ea43f84a258c59717d4539abf09f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1` - linux; amd64

```console
$ docker pull kong@sha256:e21b0b793879ab96720ed4188f9441260273f4bf775bcbff8d435e019ffb759a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49335657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cefb958bcd694597b65adc00053a762b1f9a6df3c6031af528d052d75a64e1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:10 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:10 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:10 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:10 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:10 GMT
ARG KONG_VERSION=2.8.1
# Thu, 06 Oct 2022 23:01:10 GMT
ENV KONG_VERSION=2.8.1
# Thu, 06 Oct 2022 23:01:10 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Thu, 06 Oct 2022 23:01:10 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Thu, 06 Oct 2022 23:01:17 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:18 GMT
USER kong
# Thu, 06 Oct 2022 23:01:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:18 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:18 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70653f7a2d526d9024e271d864947f47000d34d971f36a44665b51e8c3b739c`  
		Last Modified: Thu, 06 Oct 2022 23:02:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531e3bd93090d08ef911bb2c8320f2fef2428ef96597535a55111fda18efde52`  
		Last Modified: Thu, 06 Oct 2022 23:03:02 GMT  
		Size: 46.5 MB (46528590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814dd06d26c72ec884803b7dd47e90f8855d4df9267025e9eb33d22aaa061e88`  
		Last Modified: Thu, 06 Oct 2022 23:02:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8a5a7357d6cbda1840574130d109fc37b8088750d32c87b50f3b7909b7975425
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48524280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5957d67fc55af3d11bdbd87de76f7480e3c4d8bcb715d6cfd01922780f46ea9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:09 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:09 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:10 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:10 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:56:10 GMT
ARG KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:10 GMT
ENV KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:10 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Wed, 26 Oct 2022 01:56:10 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Wed, 26 Oct 2022 01:56:16 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:56:17 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:17 GMT
USER kong
# Wed, 26 Oct 2022 01:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:17 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd91e9229603b76d74826c966b221aacc86c840445a63234a9e2850a10a0062`  
		Last Modified: Wed, 26 Oct 2022 01:59:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450997ae687cb58c194a458badbbb0c90dc4aed7eab5e3b1db610305ef840dd0`  
		Last Modified: Wed, 26 Oct 2022 01:59:35 GMT  
		Size: 45.8 MB (45815605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8380bfcbd9b9294f70da613229b53465eef3ac9234edb9cbfb19006dbb36293`  
		Last Modified: Wed, 26 Oct 2022 01:59:28 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-alpine`

```console
$ docker pull kong@sha256:1b53405d8680a09d6f44494b7990bf7da2ea43f84a258c59717d4539abf09f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:e21b0b793879ab96720ed4188f9441260273f4bf775bcbff8d435e019ffb759a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49335657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cefb958bcd694597b65adc00053a762b1f9a6df3c6031af528d052d75a64e1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:01:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 06 Oct 2022 23:01:10 GMT
ARG ASSET=ce
# Thu, 06 Oct 2022 23:01:10 GMT
ENV ASSET=ce
# Thu, 06 Oct 2022 23:01:10 GMT
ARG EE_PORTS
# Thu, 06 Oct 2022 23:01:10 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 06 Oct 2022 23:01:10 GMT
ARG KONG_VERSION=2.8.1
# Thu, 06 Oct 2022 23:01:10 GMT
ENV KONG_VERSION=2.8.1
# Thu, 06 Oct 2022 23:01:10 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Thu, 06 Oct 2022 23:01:10 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Thu, 06 Oct 2022 23:01:17 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 06 Oct 2022 23:01:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 06 Oct 2022 23:01:18 GMT
USER kong
# Thu, 06 Oct 2022 23:01:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:01:18 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 06 Oct 2022 23:01:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:01:18 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 06 Oct 2022 23:01:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70653f7a2d526d9024e271d864947f47000d34d971f36a44665b51e8c3b739c`  
		Last Modified: Thu, 06 Oct 2022 23:02:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531e3bd93090d08ef911bb2c8320f2fef2428ef96597535a55111fda18efde52`  
		Last Modified: Thu, 06 Oct 2022 23:03:02 GMT  
		Size: 46.5 MB (46528590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814dd06d26c72ec884803b7dd47e90f8855d4df9267025e9eb33d22aaa061e88`  
		Last Modified: Thu, 06 Oct 2022 23:02:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8a5a7357d6cbda1840574130d109fc37b8088750d32c87b50f3b7909b7975425
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48524280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5957d67fc55af3d11bdbd87de76f7480e3c4d8bcb715d6cfd01922780f46ea9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 01:56:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 26 Oct 2022 01:56:09 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:09 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:10 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:10 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 26 Oct 2022 01:56:10 GMT
ARG KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:10 GMT
ENV KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:10 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Wed, 26 Oct 2022 01:56:10 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Wed, 26 Oct 2022 01:56:16 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 26 Oct 2022 01:56:17 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:17 GMT
USER kong
# Wed, 26 Oct 2022 01:56:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:17 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd91e9229603b76d74826c966b221aacc86c840445a63234a9e2850a10a0062`  
		Last Modified: Wed, 26 Oct 2022 01:59:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450997ae687cb58c194a458badbbb0c90dc4aed7eab5e3b1db610305ef840dd0`  
		Last Modified: Wed, 26 Oct 2022 01:59:35 GMT  
		Size: 45.8 MB (45815605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8380bfcbd9b9294f70da613229b53465eef3ac9234edb9cbfb19006dbb36293`  
		Last Modified: Wed, 26 Oct 2022 01:59:28 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-ubuntu`

```console
$ docker pull kong@sha256:9f9dddc7616066f7b02b0e1735133523502a96832f8ffcf4e83c348e99025fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:cedff6e436f88215dadcd6bf2d25062b9b5d3170ff6c9947b02c1319876e5fdb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121292578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142c60b0bbecd85bac643266c0995c1b42083af9b5c4da4d1ba31592bb7c7f8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:04:26 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:04:26 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:04:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 18:04:27 GMT
ENV KONG_VERSION=2.8.1
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Wed, 05 Oct 2022 18:04:27 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Wed, 05 Oct 2022 18:04:48 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:04:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:04:49 GMT
USER kong
# Wed, 05 Oct 2022 18:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:04:50 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:04:50 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:04:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:04:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af493d1a174862c166e0d67b32f1bb9d93e2304a59209a55e08cd858d032d8b`  
		Last Modified: Wed, 05 Oct 2022 18:07:23 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc176a053adb32647c56614ff026d0deba20cb6efd6372197e024bf7c5693e`  
		Last Modified: Wed, 05 Oct 2022 18:07:33 GMT  
		Size: 67.6 MB (67635284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69d17ca86369a39c8f6a302ebfa154002b3b253738effeb247bfa53ec0330cb`  
		Last Modified: Wed, 05 Oct 2022 18:07:21 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b3821340749f078fca49fdcf6c59874924c3bc99affad7eb4870a4c105283bd8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121736114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cd5e3353682a08855cc43120d77ffacbaba519aaf68736d4bed76ab5609ea4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:56:21 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:56:21 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:56:21 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:56:21 GMT
ARG KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:21 GMT
ENV KONG_VERSION=2.8.1
# Wed, 26 Oct 2022 01:56:21 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Wed, 26 Oct 2022 01:56:21 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Wed, 26 Oct 2022 01:56:36 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:56:37 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:38 GMT
USER kong
# Wed, 26 Oct 2022 01:56:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:38 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f13f9d5d996e141886cffb3feec65b77fb24a51d5f42dc401d608fdec73f4c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955e7d3f453f82dabe911edc9a1755176cbb03bb5422778efe0345f2afb442a2`  
		Last Modified: Wed, 26 Oct 2022 01:59:56 GMT  
		Size: 69.5 MB (69457280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae91fafd7b2bd72f523a509de3e8ae8fe69535d0bab2a8bdbd09fb0ab63dd97a`  
		Last Modified: Wed, 26 Oct 2022 01:59:47 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0`

```console
$ docker pull kong@sha256:803bda2f6c38fc042d3ac93625eec8acf1e4dec8db05566876187bb500555394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0` - linux; amd64

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

### `kong:3.0` - linux; arm64 variant v8

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

## `kong:3.0-ubuntu`

```console
$ docker pull kong@sha256:80cfb344800cf5405d204c52abf5f8b87681521ae981cebdf091d049b4192604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b94b30d589c2d304b5c32ab10ce3c5b16f58b77c2aa363583da387c335c0fb48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126751347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a998d5233b41e636a9afe797738f040dfb82731ce74c88c9208bceae5ff1c5a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:03:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Oct 2022 18:03:44 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:03:44 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ENV KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 05 Oct 2022 18:04:17 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:04:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:04:18 GMT
USER kong
# Wed, 05 Oct 2022 18:04:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:04:18 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:04:18 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:04:18 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:04:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a405c4afb98d18d76913bfe72f63dbd4a4d8c04256b6a7dfcbf44e6afba6f4`  
		Last Modified: Wed, 05 Oct 2022 18:06:58 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c61366193417348ac92ea7a0b85d3a941dd84e99ddce0ccf874f9e2dd064a6`  
		Last Modified: Wed, 05 Oct 2022 18:07:08 GMT  
		Size: 73.1 MB (73094048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff353d4dd575bdf6ca92775c17a2634b394fc8f507c04bbaedcdeee8e3eb48e`  
		Last Modified: Wed, 05 Oct 2022 18:06:56 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8e4794a5da340c86858643070b6f0770d7e7837ec86a14cb35f1ec797a1938c1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123929795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3baf9dce39994a2f6ea70ebb897661bd6acc5eef695a5a94afb90943fbc1e8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:55:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 26 Oct 2022 01:55:36 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:55:36 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:55:36 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:55:37 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:55:37 GMT
ARG KONG_VERSION=3.0.0
# Wed, 26 Oct 2022 01:55:37 GMT
ENV KONG_VERSION=3.0.0
# Wed, 26 Oct 2022 01:55:37 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 26 Oct 2022 01:55:37 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 26 Oct 2022 01:56:06 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:56:07 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:07 GMT
USER kong
# Wed, 26 Oct 2022 01:56:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:07 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbfd90e8792213bcf13933cb77f26802db6a343dfa5a8e596ec64c7b2c9c5c8`  
		Last Modified: Wed, 26 Oct 2022 01:59:07 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54267830710389ced55d1a04f28f923957268deeb68f39a0d629bc307cf49a6b`  
		Last Modified: Wed, 26 Oct 2022 01:59:16 GMT  
		Size: 71.7 MB (71650955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae2f3708ad19f0116ed1b118567d52073086e56f85f4af2cd64e963017359c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:06 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.0`

```console
$ docker pull kong@sha256:803bda2f6c38fc042d3ac93625eec8acf1e4dec8db05566876187bb500555394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.0` - linux; amd64

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

### `kong:3.0.0` - linux; arm64 variant v8

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

## `kong:3.0.0-alpine`

```console
$ docker pull kong@sha256:803bda2f6c38fc042d3ac93625eec8acf1e4dec8db05566876187bb500555394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.0-alpine` - linux; amd64

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

### `kong:3.0.0-alpine` - linux; arm64 variant v8

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

## `kong:3.0.0-ubuntu`

```console
$ docker pull kong@sha256:2c1021b89f5721657f788494341b218734dd258429740f04dcf80668ed5e3533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7c5dc0e1faae700087e0b5d100ea1e925a104511c69d927e02fcdd93d4e225da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126681693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74877fd6ac73ec1aacca102ec56550f4b7d4d978bcbd932e363a2285077ed8d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:01:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 25 Oct 2022 17:01:54 GMT
ARG ASSET=ce
# Tue, 25 Oct 2022 17:01:54 GMT
ENV ASSET=ce
# Tue, 25 Oct 2022 17:01:54 GMT
ARG EE_PORTS
# Tue, 25 Oct 2022 17:01:54 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 25 Oct 2022 17:01:55 GMT
ARG KONG_VERSION=3.0.0
# Tue, 25 Oct 2022 17:01:55 GMT
ENV KONG_VERSION=3.0.0
# Tue, 25 Oct 2022 17:01:55 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Tue, 25 Oct 2022 17:01:55 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Tue, 25 Oct 2022 17:02:26 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 25 Oct 2022 17:02:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 25 Oct 2022 17:02:27 GMT
USER kong
# Tue, 25 Oct 2022 17:02:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 17:02:27 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 25 Oct 2022 17:02:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Oct 2022 17:02:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 25 Oct 2022 17:02:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd402362b5eb17585ff21167c25c557e4f7b84cb3be167553547fd0aded947f`  
		Last Modified: Tue, 25 Oct 2022 17:05:08 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fc3892503bf1886ddf7842e00a4869a07fe7f25ffb4389e890681f31f8da2b`  
		Last Modified: Tue, 25 Oct 2022 17:05:18 GMT  
		Size: 73.0 MB (73021027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef2a5f645f0a396dd99895ca7e6fc18e548d56858cfdd2bdf6e76e595bf0ad1`  
		Last Modified: Tue, 25 Oct 2022 17:05:06 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8e4794a5da340c86858643070b6f0770d7e7837ec86a14cb35f1ec797a1938c1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123929795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3baf9dce39994a2f6ea70ebb897661bd6acc5eef695a5a94afb90943fbc1e8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:55:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 26 Oct 2022 01:55:36 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:55:36 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:55:36 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:55:37 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:55:37 GMT
ARG KONG_VERSION=3.0.0
# Wed, 26 Oct 2022 01:55:37 GMT
ENV KONG_VERSION=3.0.0
# Wed, 26 Oct 2022 01:55:37 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 26 Oct 2022 01:55:37 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 26 Oct 2022 01:56:06 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:56:07 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:07 GMT
USER kong
# Wed, 26 Oct 2022 01:56:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:07 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbfd90e8792213bcf13933cb77f26802db6a343dfa5a8e596ec64c7b2c9c5c8`  
		Last Modified: Wed, 26 Oct 2022 01:59:07 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54267830710389ced55d1a04f28f923957268deeb68f39a0d629bc307cf49a6b`  
		Last Modified: Wed, 26 Oct 2022 01:59:16 GMT  
		Size: 71.7 MB (71650955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae2f3708ad19f0116ed1b118567d52073086e56f85f4af2cd64e963017359c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:06 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:803bda2f6c38fc042d3ac93625eec8acf1e4dec8db05566876187bb500555394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

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

### `kong:alpine` - linux; arm64 variant v8

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

## `kong:ubuntu`

```console
$ docker pull kong@sha256:80cfb344800cf5405d204c52abf5f8b87681521ae981cebdf091d049b4192604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b94b30d589c2d304b5c32ab10ce3c5b16f58b77c2aa363583da387c335c0fb48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126751347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a998d5233b41e636a9afe797738f040dfb82731ce74c88c9208bceae5ff1c5a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:03:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Oct 2022 18:03:44 GMT
ARG ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ENV ASSET=ce
# Wed, 05 Oct 2022 18:03:44 GMT
ARG EE_PORTS
# Wed, 05 Oct 2022 18:03:44 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ENV KONG_VERSION=3.0.0
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 05 Oct 2022 18:03:45 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 05 Oct 2022 18:04:17 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Oct 2022 18:04:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Oct 2022 18:04:18 GMT
USER kong
# Wed, 05 Oct 2022 18:04:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 18:04:18 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Oct 2022 18:04:18 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Oct 2022 18:04:18 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Oct 2022 18:04:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a405c4afb98d18d76913bfe72f63dbd4a4d8c04256b6a7dfcbf44e6afba6f4`  
		Last Modified: Wed, 05 Oct 2022 18:06:58 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c61366193417348ac92ea7a0b85d3a941dd84e99ddce0ccf874f9e2dd064a6`  
		Last Modified: Wed, 05 Oct 2022 18:07:08 GMT  
		Size: 73.1 MB (73094048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff353d4dd575bdf6ca92775c17a2634b394fc8f507c04bbaedcdeee8e3eb48e`  
		Last Modified: Wed, 05 Oct 2022 18:06:56 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8e4794a5da340c86858643070b6f0770d7e7837ec86a14cb35f1ec797a1938c1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123929795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3baf9dce39994a2f6ea70ebb897661bd6acc5eef695a5a94afb90943fbc1e8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:55:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 26 Oct 2022 01:55:36 GMT
ARG ASSET=ce
# Wed, 26 Oct 2022 01:55:36 GMT
ENV ASSET=ce
# Wed, 26 Oct 2022 01:55:36 GMT
ARG EE_PORTS
# Wed, 26 Oct 2022 01:55:37 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 26 Oct 2022 01:55:37 GMT
ARG KONG_VERSION=3.0.0
# Wed, 26 Oct 2022 01:55:37 GMT
ENV KONG_VERSION=3.0.0
# Wed, 26 Oct 2022 01:55:37 GMT
ARG KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d
# Wed, 26 Oct 2022 01:55:37 GMT
ARG KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
# Wed, 26 Oct 2022 01:56:06 GMT
# ARGS: KONG_AMD64_SHA=3a38f6c4ba1cfc8897e655e46b957c7b0f2dd930111bf3d02411fedd1de53d6d KONG_ARM64_SHA=190f82dd47df19339c025f37701e62191aa3063e77e15c5e57d5b77869058f69
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 26 Oct 2022 01:56:07 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 26 Oct 2022 01:56:07 GMT
USER kong
# Wed, 26 Oct 2022 01:56:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Oct 2022 01:56:07 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 26 Oct 2022 01:56:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:56:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 26 Oct 2022 01:56:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbfd90e8792213bcf13933cb77f26802db6a343dfa5a8e596ec64c7b2c9c5c8`  
		Last Modified: Wed, 26 Oct 2022 01:59:07 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54267830710389ced55d1a04f28f923957268deeb68f39a0d629bc307cf49a6b`  
		Last Modified: Wed, 26 Oct 2022 01:59:16 GMT  
		Size: 71.7 MB (71650955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae2f3708ad19f0116ed1b118567d52073086e56f85f4af2cd64e963017359c5`  
		Last Modified: Wed, 26 Oct 2022 01:59:06 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
