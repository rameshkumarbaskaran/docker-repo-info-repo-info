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
-	[`kong:2.8.3`](#kong283)
-	[`kong:2.8.3-alpine`](#kong283-alpine)
-	[`kong:2.8.3-ubuntu`](#kong283-ubuntu)
-	[`kong:3`](#kong3)
-	[`kong:3.0`](#kong30)
-	[`kong:3.0-alpine`](#kong30-alpine)
-	[`kong:3.0-ubuntu`](#kong30-ubuntu)
-	[`kong:3.0.1`](#kong301)
-	[`kong:3.0.1-alpine`](#kong301-alpine)
-	[`kong:3.0.1-ubuntu`](#kong301-ubuntu)
-	[`kong:3.1`](#kong31)
-	[`kong:3.1-ubuntu`](#kong31-ubuntu)
-	[`kong:3.1.0`](#kong310)
-	[`kong:3.1.0-alpine`](#kong310-alpine)
-	[`kong:3.1.0-ubuntu`](#kong310-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.5`

```console
$ docker pull kong@sha256:4d459bf9f353e69df80d660a7544d29583e77d5292f827137f6add87f74d2364
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
$ docker pull kong@sha256:934f0f609894a62d5ab41685863f02b29e7aa7d454b8e00482ed493fa32aaed1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48391762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddbd7a976f9e47f0c736179c4fe225a32899cb86cebf1dd093bf993018a77e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:40:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 10 Nov 2022 22:40:04 GMT
ARG ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ENV ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 22:40:04 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 10 Nov 2022 22:40:29 GMT
ARG KONG_VERSION=2.5.2
# Thu, 10 Nov 2022 22:40:29 GMT
ENV KONG_VERSION=2.5.2
# Thu, 10 Nov 2022 22:40:29 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Thu, 10 Nov 2022 22:40:29 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Thu, 10 Nov 2022 22:40:35 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 10 Nov 2022 22:40:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 22:40:35 GMT
USER kong
# Thu, 10 Nov 2022 22:40:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 22:40:36 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 22:40:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 22:40:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 22:40:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f5eba777c2192f562d24cd3da16152dec7d8942677370e1524b03a6e36a2b`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578c76f657afd39a075841d957e371975dda66e218c2055e95e692d64aa969ee`  
		Last Modified: Thu, 10 Nov 2022 22:42:47 GMT  
		Size: 45.7 MB (45672316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ad9797993253de6ac3a029a742d251a5445f0acc9ac38af3e937ae07078d3f`  
		Last Modified: Thu, 10 Nov 2022 22:42:40 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:78408c5b76808d0da2f03fbbfecfd8f78b6cffc69500b7722b51da40d427eb9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:97c760f470e55d20889eed02eadcbb066b386bd2f44cc764e259baa6f62b6328
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121316956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad73138d2da5fd9ef9e47f093a2042de3aec15e9bdce9db8a5d5e60d60cd835`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:21:05 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:21:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:22:06 GMT
ARG KONG_VERSION=2.5.2
# Fri, 09 Dec 2022 02:22:06 GMT
ENV KONG_VERSION=2.5.2
# Fri, 09 Dec 2022 02:22:06 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Fri, 09 Dec 2022 02:22:06 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Fri, 09 Dec 2022 02:22:26 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:22:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:22:27 GMT
USER kong
# Fri, 09 Dec 2022 02:22:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:22:27 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:22:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:22:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:22:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6580311fe457a0b6cc8ae95087c3a921a45c32aa153828bd82215f2d34b87788`  
		Last Modified: Fri, 09 Dec 2022 02:24:18 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dca52dfdcdb7c5d2d2c18c52b2bdd389c39df2ca110b22f88392f8dd31dc62`  
		Last Modified: Fri, 09 Dec 2022 02:25:12 GMT  
		Size: 67.7 MB (67657224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd0fa79fc5bb9fa06e91b8544c75b88e550240c68fa79e4db7903a0a04d5ca`  
		Last Modified: Fri, 09 Dec 2022 02:25:01 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5fb42ef6702e69f6f83bbeb62426f65f4954218fbfb214480eb0466a2f918fb1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43a86fd06613c7fb6f90f8e2ff34a63178106e556ce14c6c0c0d8b4534a4996`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:46:53 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:46:53 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:47:36 GMT
ARG KONG_VERSION=2.5.2
# Fri, 09 Dec 2022 04:47:36 GMT
ENV KONG_VERSION=2.5.2
# Fri, 09 Dec 2022 04:47:36 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Fri, 09 Dec 2022 04:47:36 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Fri, 09 Dec 2022 04:47:51 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:47:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:47:52 GMT
USER kong
# Fri, 09 Dec 2022 04:47:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:47:52 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:47:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:47:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:47:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eef6633ff913692206949a1678c2823f245d29b9beb566b91495e75fbbcd99`  
		Last Modified: Fri, 09 Dec 2022 04:49:12 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007f41795294938930d1ae557c5f8a407e7e4c02eb85b8a117c82a2deabbd48f`  
		Last Modified: Fri, 09 Dec 2022 04:49:59 GMT  
		Size: 66.1 MB (66072184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e64c1a0d638ce451e81c243878b5b3cfec87110ba617b544df0f00f2a3e8717`  
		Last Modified: Fri, 09 Dec 2022 04:49:50 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2`

```console
$ docker pull kong@sha256:4d459bf9f353e69df80d660a7544d29583e77d5292f827137f6add87f74d2364
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
$ docker pull kong@sha256:934f0f609894a62d5ab41685863f02b29e7aa7d454b8e00482ed493fa32aaed1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48391762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddbd7a976f9e47f0c736179c4fe225a32899cb86cebf1dd093bf993018a77e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:40:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 10 Nov 2022 22:40:04 GMT
ARG ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ENV ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 22:40:04 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 10 Nov 2022 22:40:29 GMT
ARG KONG_VERSION=2.5.2
# Thu, 10 Nov 2022 22:40:29 GMT
ENV KONG_VERSION=2.5.2
# Thu, 10 Nov 2022 22:40:29 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Thu, 10 Nov 2022 22:40:29 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Thu, 10 Nov 2022 22:40:35 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 10 Nov 2022 22:40:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 22:40:35 GMT
USER kong
# Thu, 10 Nov 2022 22:40:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 22:40:36 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 22:40:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 22:40:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 22:40:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f5eba777c2192f562d24cd3da16152dec7d8942677370e1524b03a6e36a2b`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578c76f657afd39a075841d957e371975dda66e218c2055e95e692d64aa969ee`  
		Last Modified: Thu, 10 Nov 2022 22:42:47 GMT  
		Size: 45.7 MB (45672316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ad9797993253de6ac3a029a742d251a5445f0acc9ac38af3e937ae07078d3f`  
		Last Modified: Thu, 10 Nov 2022 22:42:40 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-alpine`

```console
$ docker pull kong@sha256:4d459bf9f353e69df80d660a7544d29583e77d5292f827137f6add87f74d2364
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
$ docker pull kong@sha256:934f0f609894a62d5ab41685863f02b29e7aa7d454b8e00482ed493fa32aaed1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48391762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddbd7a976f9e47f0c736179c4fe225a32899cb86cebf1dd093bf993018a77e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:40:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 10 Nov 2022 22:40:04 GMT
ARG ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ENV ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 22:40:04 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 10 Nov 2022 22:40:29 GMT
ARG KONG_VERSION=2.5.2
# Thu, 10 Nov 2022 22:40:29 GMT
ENV KONG_VERSION=2.5.2
# Thu, 10 Nov 2022 22:40:29 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Thu, 10 Nov 2022 22:40:29 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Thu, 10 Nov 2022 22:40:35 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 10 Nov 2022 22:40:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 22:40:35 GMT
USER kong
# Thu, 10 Nov 2022 22:40:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 22:40:36 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 22:40:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 22:40:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 22:40:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f5eba777c2192f562d24cd3da16152dec7d8942677370e1524b03a6e36a2b`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578c76f657afd39a075841d957e371975dda66e218c2055e95e692d64aa969ee`  
		Last Modified: Thu, 10 Nov 2022 22:42:47 GMT  
		Size: 45.7 MB (45672316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ad9797993253de6ac3a029a742d251a5445f0acc9ac38af3e937ae07078d3f`  
		Last Modified: Thu, 10 Nov 2022 22:42:40 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-ubuntu`

```console
$ docker pull kong@sha256:78408c5b76808d0da2f03fbbfecfd8f78b6cffc69500b7722b51da40d427eb9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:97c760f470e55d20889eed02eadcbb066b386bd2f44cc764e259baa6f62b6328
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121316956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad73138d2da5fd9ef9e47f093a2042de3aec15e9bdce9db8a5d5e60d60cd835`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:21:05 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:21:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:22:06 GMT
ARG KONG_VERSION=2.5.2
# Fri, 09 Dec 2022 02:22:06 GMT
ENV KONG_VERSION=2.5.2
# Fri, 09 Dec 2022 02:22:06 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Fri, 09 Dec 2022 02:22:06 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Fri, 09 Dec 2022 02:22:26 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:22:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:22:27 GMT
USER kong
# Fri, 09 Dec 2022 02:22:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:22:27 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:22:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:22:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:22:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6580311fe457a0b6cc8ae95087c3a921a45c32aa153828bd82215f2d34b87788`  
		Last Modified: Fri, 09 Dec 2022 02:24:18 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dca52dfdcdb7c5d2d2c18c52b2bdd389c39df2ca110b22f88392f8dd31dc62`  
		Last Modified: Fri, 09 Dec 2022 02:25:12 GMT  
		Size: 67.7 MB (67657224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd0fa79fc5bb9fa06e91b8544c75b88e550240c68fa79e4db7903a0a04d5ca`  
		Last Modified: Fri, 09 Dec 2022 02:25:01 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5fb42ef6702e69f6f83bbeb62426f65f4954218fbfb214480eb0466a2f918fb1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43a86fd06613c7fb6f90f8e2ff34a63178106e556ce14c6c0c0d8b4534a4996`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:46:53 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:46:53 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:47:36 GMT
ARG KONG_VERSION=2.5.2
# Fri, 09 Dec 2022 04:47:36 GMT
ENV KONG_VERSION=2.5.2
# Fri, 09 Dec 2022 04:47:36 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Fri, 09 Dec 2022 04:47:36 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Fri, 09 Dec 2022 04:47:51 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:47:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:47:52 GMT
USER kong
# Fri, 09 Dec 2022 04:47:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:47:52 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:47:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:47:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:47:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eef6633ff913692206949a1678c2823f245d29b9beb566b91495e75fbbcd99`  
		Last Modified: Fri, 09 Dec 2022 04:49:12 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007f41795294938930d1ae557c5f8a407e7e4c02eb85b8a117c82a2deabbd48f`  
		Last Modified: Fri, 09 Dec 2022 04:49:59 GMT  
		Size: 66.1 MB (66072184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e64c1a0d638ce451e81c243878b5b3cfec87110ba617b544df0f00f2a3e8717`  
		Last Modified: Fri, 09 Dec 2022 04:49:50 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:62eb6d17133b007cbf5831b39197c669b8700c55283270395b876d1ecfd69a70
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
$ docker pull kong@sha256:607d9bdc48adf88bcee03b5dfa77a2d7d8293c803e12c97c897a129b27e6a669
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49626411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119c7b9aedaeb47ed122d6ec970ab5c7214b29169221bfdb9cfe7a7602e49454`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:40:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 10 Nov 2022 22:40:04 GMT
ARG ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ENV ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 22:40:04 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 10 Nov 2022 22:40:17 GMT
ARG KONG_VERSION=2.6.1
# Thu, 10 Nov 2022 22:40:17 GMT
ENV KONG_VERSION=2.6.1
# Thu, 10 Nov 2022 22:40:18 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Thu, 10 Nov 2022 22:40:18 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Thu, 10 Nov 2022 22:40:23 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 10 Nov 2022 22:40:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 22:40:24 GMT
USER kong
# Thu, 10 Nov 2022 22:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 22:40:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 22:40:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 22:40:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 22:40:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f5eba777c2192f562d24cd3da16152dec7d8942677370e1524b03a6e36a2b`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dc6c1f293dd1473f1dd7e3176777c7089b6bdcebd2c879cbc2a0040daf2bf2`  
		Last Modified: Thu, 10 Nov 2022 22:42:28 GMT  
		Size: 46.9 MB (46906964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7605604f20571f531c42364dbfc0858fe97409b5faa3f8407a409e04c2946b7`  
		Last Modified: Thu, 10 Nov 2022 22:42:21 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:451cfefd00ac3640bd84008fd774cf65832695cd2c092044a0b153138b356cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:4233f855079cb1ea7c01b97a27c0990dea3892de1ec9d30dd66f05dfd76f096d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128203862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3370ce63be78455e952e7c714097a5e8cf6a551b1d4a20a825c00e52d923d838`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:21:05 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:21:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:21:35 GMT
ARG KONG_VERSION=2.6.1
# Fri, 09 Dec 2022 02:21:35 GMT
ENV KONG_VERSION=2.6.1
# Fri, 09 Dec 2022 02:21:36 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Fri, 09 Dec 2022 02:21:36 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Fri, 09 Dec 2022 02:21:56 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:21:57 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:21:57 GMT
USER kong
# Fri, 09 Dec 2022 02:21:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:21:57 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:21:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:21:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:21:58 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6580311fe457a0b6cc8ae95087c3a921a45c32aa153828bd82215f2d34b87788`  
		Last Modified: Fri, 09 Dec 2022 02:24:18 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea46aaa433792c4b80f172a7f26f23bcfc0779a15354bae452f23e4b84d3a7e`  
		Last Modified: Fri, 09 Dec 2022 02:24:51 GMT  
		Size: 74.5 MB (74544130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190e3771c033e41b3563fc9f0742bdc9568b37ccff7b84b2e3b387424e5894d`  
		Last Modified: Fri, 09 Dec 2022 02:24:39 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:343ffa6c1152318285018a0f8091af8118c7e9dcc8156201d85e98dca70ce2af
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125246509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52639dfaf63a6e81b1d690b1ee2b89ad042b1a946bb62924c7a8a3b402ee0c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:46:53 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:46:53 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:47:14 GMT
ARG KONG_VERSION=2.6.1
# Fri, 09 Dec 2022 04:47:14 GMT
ENV KONG_VERSION=2.6.1
# Fri, 09 Dec 2022 04:47:14 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Fri, 09 Dec 2022 04:47:14 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Fri, 09 Dec 2022 04:47:30 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:47:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:47:32 GMT
USER kong
# Fri, 09 Dec 2022 04:47:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:47:32 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:47:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:47:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:47:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eef6633ff913692206949a1678c2823f245d29b9beb566b91495e75fbbcd99`  
		Last Modified: Fri, 09 Dec 2022 04:49:12 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffe292ba5b9aa2b8eaccd17fb25cf33a07d4de3ecb9f8a13ddc16a757aa90ee`  
		Last Modified: Fri, 09 Dec 2022 04:49:40 GMT  
		Size: 73.0 MB (72970506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4fe1c5229da775bb18809a3c71f604e67b69b936529abcca6b55a8dec6316b`  
		Last Modified: Fri, 09 Dec 2022 04:49:30 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1`

```console
$ docker pull kong@sha256:62eb6d17133b007cbf5831b39197c669b8700c55283270395b876d1ecfd69a70
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
$ docker pull kong@sha256:607d9bdc48adf88bcee03b5dfa77a2d7d8293c803e12c97c897a129b27e6a669
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49626411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119c7b9aedaeb47ed122d6ec970ab5c7214b29169221bfdb9cfe7a7602e49454`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:40:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 10 Nov 2022 22:40:04 GMT
ARG ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ENV ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 22:40:04 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 10 Nov 2022 22:40:17 GMT
ARG KONG_VERSION=2.6.1
# Thu, 10 Nov 2022 22:40:17 GMT
ENV KONG_VERSION=2.6.1
# Thu, 10 Nov 2022 22:40:18 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Thu, 10 Nov 2022 22:40:18 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Thu, 10 Nov 2022 22:40:23 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 10 Nov 2022 22:40:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 22:40:24 GMT
USER kong
# Thu, 10 Nov 2022 22:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 22:40:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 22:40:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 22:40:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 22:40:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f5eba777c2192f562d24cd3da16152dec7d8942677370e1524b03a6e36a2b`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dc6c1f293dd1473f1dd7e3176777c7089b6bdcebd2c879cbc2a0040daf2bf2`  
		Last Modified: Thu, 10 Nov 2022 22:42:28 GMT  
		Size: 46.9 MB (46906964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7605604f20571f531c42364dbfc0858fe97409b5faa3f8407a409e04c2946b7`  
		Last Modified: Thu, 10 Nov 2022 22:42:21 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-alpine`

```console
$ docker pull kong@sha256:62eb6d17133b007cbf5831b39197c669b8700c55283270395b876d1ecfd69a70
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
$ docker pull kong@sha256:607d9bdc48adf88bcee03b5dfa77a2d7d8293c803e12c97c897a129b27e6a669
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49626411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119c7b9aedaeb47ed122d6ec970ab5c7214b29169221bfdb9cfe7a7602e49454`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:40:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 10 Nov 2022 22:40:04 GMT
ARG ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ENV ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 22:40:04 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 10 Nov 2022 22:40:17 GMT
ARG KONG_VERSION=2.6.1
# Thu, 10 Nov 2022 22:40:17 GMT
ENV KONG_VERSION=2.6.1
# Thu, 10 Nov 2022 22:40:18 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Thu, 10 Nov 2022 22:40:18 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Thu, 10 Nov 2022 22:40:23 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 10 Nov 2022 22:40:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 22:40:24 GMT
USER kong
# Thu, 10 Nov 2022 22:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 22:40:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 22:40:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 22:40:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 22:40:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f5eba777c2192f562d24cd3da16152dec7d8942677370e1524b03a6e36a2b`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dc6c1f293dd1473f1dd7e3176777c7089b6bdcebd2c879cbc2a0040daf2bf2`  
		Last Modified: Thu, 10 Nov 2022 22:42:28 GMT  
		Size: 46.9 MB (46906964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7605604f20571f531c42364dbfc0858fe97409b5faa3f8407a409e04c2946b7`  
		Last Modified: Thu, 10 Nov 2022 22:42:21 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-ubuntu`

```console
$ docker pull kong@sha256:451cfefd00ac3640bd84008fd774cf65832695cd2c092044a0b153138b356cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:4233f855079cb1ea7c01b97a27c0990dea3892de1ec9d30dd66f05dfd76f096d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128203862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3370ce63be78455e952e7c714097a5e8cf6a551b1d4a20a825c00e52d923d838`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:21:05 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:21:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:21:35 GMT
ARG KONG_VERSION=2.6.1
# Fri, 09 Dec 2022 02:21:35 GMT
ENV KONG_VERSION=2.6.1
# Fri, 09 Dec 2022 02:21:36 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Fri, 09 Dec 2022 02:21:36 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Fri, 09 Dec 2022 02:21:56 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:21:57 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:21:57 GMT
USER kong
# Fri, 09 Dec 2022 02:21:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:21:57 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:21:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:21:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:21:58 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6580311fe457a0b6cc8ae95087c3a921a45c32aa153828bd82215f2d34b87788`  
		Last Modified: Fri, 09 Dec 2022 02:24:18 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea46aaa433792c4b80f172a7f26f23bcfc0779a15354bae452f23e4b84d3a7e`  
		Last Modified: Fri, 09 Dec 2022 02:24:51 GMT  
		Size: 74.5 MB (74544130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190e3771c033e41b3563fc9f0742bdc9568b37ccff7b84b2e3b387424e5894d`  
		Last Modified: Fri, 09 Dec 2022 02:24:39 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:343ffa6c1152318285018a0f8091af8118c7e9dcc8156201d85e98dca70ce2af
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125246509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52639dfaf63a6e81b1d690b1ee2b89ad042b1a946bb62924c7a8a3b402ee0c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:46:53 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:46:53 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:47:14 GMT
ARG KONG_VERSION=2.6.1
# Fri, 09 Dec 2022 04:47:14 GMT
ENV KONG_VERSION=2.6.1
# Fri, 09 Dec 2022 04:47:14 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Fri, 09 Dec 2022 04:47:14 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Fri, 09 Dec 2022 04:47:30 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:47:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:47:32 GMT
USER kong
# Fri, 09 Dec 2022 04:47:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:47:32 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:47:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:47:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:47:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eef6633ff913692206949a1678c2823f245d29b9beb566b91495e75fbbcd99`  
		Last Modified: Fri, 09 Dec 2022 04:49:12 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffe292ba5b9aa2b8eaccd17fb25cf33a07d4de3ecb9f8a13ddc16a757aa90ee`  
		Last Modified: Fri, 09 Dec 2022 04:49:40 GMT  
		Size: 73.0 MB (72970506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4fe1c5229da775bb18809a3c71f604e67b69b936529abcca6b55a8dec6316b`  
		Last Modified: Fri, 09 Dec 2022 04:49:30 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7`

```console
$ docker pull kong@sha256:95cbba86c8addbfee6726b5a7743ab9bb8158c4a801caa75aafe3fe03992f170
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
$ docker pull kong@sha256:7c35b5df861fc05fc12db8f1c7f98f5b07d1490f9bce31d0a58edea1098c466c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3bd472c5d632ebf186555ef7b7d99ef7ba814308a256a1ec8a7367f9924db7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:40:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 10 Nov 2022 22:40:04 GMT
ARG ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ENV ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 22:40:04 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 10 Nov 2022 22:40:05 GMT
ARG KONG_VERSION=2.7.2
# Thu, 10 Nov 2022 22:40:05 GMT
ENV KONG_VERSION=2.7.2
# Thu, 10 Nov 2022 22:40:05 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Thu, 10 Nov 2022 22:40:05 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Thu, 10 Nov 2022 22:40:11 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 10 Nov 2022 22:40:12 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 22:40:12 GMT
USER kong
# Thu, 10 Nov 2022 22:40:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 22:40:12 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 22:40:12 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 22:40:12 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 22:40:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f5eba777c2192f562d24cd3da16152dec7d8942677370e1524b03a6e36a2b`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14140154bb3de6de0062d495454ecbf830c029091e8d80c241b3d684de9e2f6f`  
		Last Modified: Thu, 10 Nov 2022 22:42:05 GMT  
		Size: 46.8 MB (46825491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7424b484ab8703ef3d0f7813540b8ce7e9de2dc487b6d9ae31593abecc0b9f44`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7-ubuntu`

```console
$ docker pull kong@sha256:556ae5906b41ea3f6e38fc4cd1d39dc2ad86538a5b12308fbad694b1d4c8ea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6e5fa94e7a30112bef9b624f1fda23df50c87b2bce1c3428827de6d1b82f45d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128109079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9331b661e2a5c3ed491501184cd8e76d34620f972b64be4f1d155608093e9679`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:21:05 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:21:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:21:06 GMT
ARG KONG_VERSION=2.7.2
# Fri, 09 Dec 2022 02:21:06 GMT
ENV KONG_VERSION=2.7.2
# Fri, 09 Dec 2022 02:21:06 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Fri, 09 Dec 2022 02:21:06 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Fri, 09 Dec 2022 02:21:27 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:21:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:21:28 GMT
USER kong
# Fri, 09 Dec 2022 02:21:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:21:28 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:21:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:21:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:21:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6580311fe457a0b6cc8ae95087c3a921a45c32aa153828bd82215f2d34b87788`  
		Last Modified: Fri, 09 Dec 2022 02:24:18 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc6150aab59bc717c083744e10ce7a9cc309858a2f11d193a6ae731eceb3e99`  
		Last Modified: Fri, 09 Dec 2022 02:24:29 GMT  
		Size: 74.4 MB (74449347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba4fe048330c6757f017dae15cc99148381947504ce42c37f2db8b001be9760`  
		Last Modified: Fri, 09 Dec 2022 02:24:17 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e53489a24cb397c62b8384ae591085b4d54068c2dee6e3ed8110c77fb688b042
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125164197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfab591a7a3122734a1d40e1234334f91028033b55815017e2ed32976e3b2d54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:46:53 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:46:53 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:46:53 GMT
ARG KONG_VERSION=2.7.2
# Fri, 09 Dec 2022 04:46:53 GMT
ENV KONG_VERSION=2.7.2
# Fri, 09 Dec 2022 04:46:53 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Fri, 09 Dec 2022 04:46:53 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Fri, 09 Dec 2022 04:47:09 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:47:10 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:47:10 GMT
USER kong
# Fri, 09 Dec 2022 04:47:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:47:10 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:47:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:47:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:47:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eef6633ff913692206949a1678c2823f245d29b9beb566b91495e75fbbcd99`  
		Last Modified: Fri, 09 Dec 2022 04:49:12 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cead60aa8a374c5c1c8a24b33a9244e04bbbe2fa8273370c7ee3e14d5d6df0e`  
		Last Modified: Fri, 09 Dec 2022 04:49:21 GMT  
		Size: 72.9 MB (72888193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840c1122d8edcfe61552299a5737e8210bb1177c892a50e585a5bff6954636f9`  
		Last Modified: Fri, 09 Dec 2022 04:49:11 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2`

```console
$ docker pull kong@sha256:95cbba86c8addbfee6726b5a7743ab9bb8158c4a801caa75aafe3fe03992f170
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
$ docker pull kong@sha256:7c35b5df861fc05fc12db8f1c7f98f5b07d1490f9bce31d0a58edea1098c466c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3bd472c5d632ebf186555ef7b7d99ef7ba814308a256a1ec8a7367f9924db7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:40:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 10 Nov 2022 22:40:04 GMT
ARG ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ENV ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 22:40:04 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 10 Nov 2022 22:40:05 GMT
ARG KONG_VERSION=2.7.2
# Thu, 10 Nov 2022 22:40:05 GMT
ENV KONG_VERSION=2.7.2
# Thu, 10 Nov 2022 22:40:05 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Thu, 10 Nov 2022 22:40:05 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Thu, 10 Nov 2022 22:40:11 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 10 Nov 2022 22:40:12 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 22:40:12 GMT
USER kong
# Thu, 10 Nov 2022 22:40:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 22:40:12 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 22:40:12 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 22:40:12 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 22:40:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f5eba777c2192f562d24cd3da16152dec7d8942677370e1524b03a6e36a2b`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14140154bb3de6de0062d495454ecbf830c029091e8d80c241b3d684de9e2f6f`  
		Last Modified: Thu, 10 Nov 2022 22:42:05 GMT  
		Size: 46.8 MB (46825491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7424b484ab8703ef3d0f7813540b8ce7e9de2dc487b6d9ae31593abecc0b9f44`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-alpine`

```console
$ docker pull kong@sha256:95cbba86c8addbfee6726b5a7743ab9bb8158c4a801caa75aafe3fe03992f170
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
$ docker pull kong@sha256:7c35b5df861fc05fc12db8f1c7f98f5b07d1490f9bce31d0a58edea1098c466c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3bd472c5d632ebf186555ef7b7d99ef7ba814308a256a1ec8a7367f9924db7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 22:40:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 10 Nov 2022 22:40:04 GMT
ARG ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ENV ASSET=ce
# Thu, 10 Nov 2022 22:40:04 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 22:40:04 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 10 Nov 2022 22:40:05 GMT
ARG KONG_VERSION=2.7.2
# Thu, 10 Nov 2022 22:40:05 GMT
ENV KONG_VERSION=2.7.2
# Thu, 10 Nov 2022 22:40:05 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Thu, 10 Nov 2022 22:40:05 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Thu, 10 Nov 2022 22:40:11 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 10 Nov 2022 22:40:12 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 22:40:12 GMT
USER kong
# Thu, 10 Nov 2022 22:40:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 22:40:12 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 22:40:12 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 22:40:12 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 22:40:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9f5eba777c2192f562d24cd3da16152dec7d8942677370e1524b03a6e36a2b`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14140154bb3de6de0062d495454ecbf830c029091e8d80c241b3d684de9e2f6f`  
		Last Modified: Thu, 10 Nov 2022 22:42:05 GMT  
		Size: 46.8 MB (46825491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7424b484ab8703ef3d0f7813540b8ce7e9de2dc487b6d9ae31593abecc0b9f44`  
		Last Modified: Thu, 10 Nov 2022 22:41:58 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-ubuntu`

```console
$ docker pull kong@sha256:556ae5906b41ea3f6e38fc4cd1d39dc2ad86538a5b12308fbad694b1d4c8ea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6e5fa94e7a30112bef9b624f1fda23df50c87b2bce1c3428827de6d1b82f45d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128109079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9331b661e2a5c3ed491501184cd8e76d34620f972b64be4f1d155608093e9679`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:21:05 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:21:05 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:21:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:21:06 GMT
ARG KONG_VERSION=2.7.2
# Fri, 09 Dec 2022 02:21:06 GMT
ENV KONG_VERSION=2.7.2
# Fri, 09 Dec 2022 02:21:06 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Fri, 09 Dec 2022 02:21:06 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Fri, 09 Dec 2022 02:21:27 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:21:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:21:28 GMT
USER kong
# Fri, 09 Dec 2022 02:21:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:21:28 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:21:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:21:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:21:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6580311fe457a0b6cc8ae95087c3a921a45c32aa153828bd82215f2d34b87788`  
		Last Modified: Fri, 09 Dec 2022 02:24:18 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc6150aab59bc717c083744e10ce7a9cc309858a2f11d193a6ae731eceb3e99`  
		Last Modified: Fri, 09 Dec 2022 02:24:29 GMT  
		Size: 74.4 MB (74449347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba4fe048330c6757f017dae15cc99148381947504ce42c37f2db8b001be9760`  
		Last Modified: Fri, 09 Dec 2022 02:24:17 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e53489a24cb397c62b8384ae591085b4d54068c2dee6e3ed8110c77fb688b042
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125164197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfab591a7a3122734a1d40e1234334f91028033b55815017e2ed32976e3b2d54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:46:53 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:46:53 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:46:53 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:46:53 GMT
ARG KONG_VERSION=2.7.2
# Fri, 09 Dec 2022 04:46:53 GMT
ENV KONG_VERSION=2.7.2
# Fri, 09 Dec 2022 04:46:53 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Fri, 09 Dec 2022 04:46:53 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Fri, 09 Dec 2022 04:47:09 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:47:10 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:47:10 GMT
USER kong
# Fri, 09 Dec 2022 04:47:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:47:10 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:47:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:47:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:47:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eef6633ff913692206949a1678c2823f245d29b9beb566b91495e75fbbcd99`  
		Last Modified: Fri, 09 Dec 2022 04:49:12 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cead60aa8a374c5c1c8a24b33a9244e04bbbe2fa8273370c7ee3e14d5d6df0e`  
		Last Modified: Fri, 09 Dec 2022 04:49:21 GMT  
		Size: 72.9 MB (72888193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840c1122d8edcfe61552299a5737e8210bb1177c892a50e585a5bff6954636f9`  
		Last Modified: Fri, 09 Dec 2022 04:49:11 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8`

```console
$ docker pull kong@sha256:c4b2838a87f28dda665fc52cd57b2e4956c3012cc6d60bef9ab15b8b474a3588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:a8eb48a7e0b6a6231f4f44f8e0ec795dd322b44c7004dc00922862dad7d68199
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49335332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a4481ac0d615c6a0ae74e00fa1e67ac5efbe29eb4429e696bd6020f6fb919e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 12 Nov 2022 08:33:20 GMT
ARG ASSET=ce
# Sat, 12 Nov 2022 08:33:20 GMT
ENV ASSET=ce
# Sat, 12 Nov 2022 08:33:20 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 08:33:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 12 Nov 2022 08:33:20 GMT
ARG KONG_VERSION=2.8.3
# Sat, 12 Nov 2022 08:33:20 GMT
ENV KONG_VERSION=2.8.3
# Sat, 12 Nov 2022 08:33:20 GMT
ARG KONG_AMD64_SHA=962ac92c9834cb59f1d6563412714f3d6eecfe6c6849a84cfcbe7a4b3facbf46
# Sat, 12 Nov 2022 08:33:20 GMT
ARG KONG_ARM64_SHA=7076e6ee6a03df86795a1a08cf86e0349a150095e61be266db462cb7de9fd745
# Sat, 12 Nov 2022 08:33:27 GMT
# ARGS: KONG_AMD64_SHA=962ac92c9834cb59f1d6563412714f3d6eecfe6c6849a84cfcbe7a4b3facbf46 KONG_ARM64_SHA=7076e6ee6a03df86795a1a08cf86e0349a150095e61be266db462cb7de9fd745
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 12 Nov 2022 08:33:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 08:33:28 GMT
USER kong
# Sat, 12 Nov 2022 08:33:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:33:28 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 08:33:28 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 08:33:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 08:33:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb280baa9a48dcb41479263bee3784fcbf4fd49e55fb1ce556437aac0a14f66e`  
		Last Modified: Sat, 12 Nov 2022 08:34:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a483e5d82932b46ee26095c1122af40655ec240003f002ade98f3ef69ab4bcf`  
		Last Modified: Sat, 12 Nov 2022 08:34:50 GMT  
		Size: 46.5 MB (46528047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0809b8d4226790980e9e9596b9ebf2858c446e3db58b4f87d07ffe23495c750e`  
		Last Modified: Sat, 12 Nov 2022 08:34:42 GMT  
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
$ docker pull kong@sha256:d26fa7e914b64c49187ca04c0ed1b08d7cc3a008f1d0b07f6790a9a4e927e4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:027f3304be0620a44e95c313bbb2ec683f42fb0f077433e958fd8542cab49439
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119163850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f3625d05e9a144ab3a04ddc2827252120d95bb1c15ce093e45c2c190c0aa32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:20:29 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:20:29 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:20:29 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:20:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:20:30 GMT
ARG KONG_VERSION=2.8.3
# Fri, 09 Dec 2022 02:20:30 GMT
ENV KONG_VERSION=2.8.3
# Fri, 09 Dec 2022 02:20:30 GMT
ARG KONG_AMD64_SHA=897e159da8e1432e474794d1e25d81fe6548adfa7b68beb186365d732e031d63
# Fri, 09 Dec 2022 02:20:30 GMT
ARG KONG_ARM64_SHA=5f806a19dcb3f4f41108fd6472a2480c7f6032519ecb506de5c9da8a0faf8172
# Fri, 09 Dec 2022 02:20:58 GMT
# ARGS: KONG_AMD64_SHA=897e159da8e1432e474794d1e25d81fe6548adfa7b68beb186365d732e031d63 KONG_ARM64_SHA=5f806a19dcb3f4f41108fd6472a2480c7f6032519ecb506de5c9da8a0faf8172
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:20:58 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:20:58 GMT
USER kong
# Fri, 09 Dec 2022 02:20:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:20:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:20:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:20:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:20:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2474cb36d2a55205f237b1c32237602452e0ed8d89aef167678418cc2273d`  
		Last Modified: Fri, 09 Dec 2022 02:23:57 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c75b22921c0bbb0198757ae391953d69cff9bb88e2a1766b12b6d618bde261`  
		Last Modified: Fri, 09 Dec 2022 02:24:07 GMT  
		Size: 67.4 MB (67369548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c182791e4fe2c7484fa0448513d9d9bd02a5061dc761c0daf005b847b8f79f`  
		Last Modified: Fri, 09 Dec 2022 02:23:56 GMT  
		Size: 881.0 B  
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

## `kong:2.8.3`

```console
$ docker pull kong@sha256:52ba05e86adcc19d7409c82840fee3773d84f3ff9f768832459af78914aeafb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.3` - linux; amd64

```console
$ docker pull kong@sha256:a8eb48a7e0b6a6231f4f44f8e0ec795dd322b44c7004dc00922862dad7d68199
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49335332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a4481ac0d615c6a0ae74e00fa1e67ac5efbe29eb4429e696bd6020f6fb919e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 12 Nov 2022 08:33:20 GMT
ARG ASSET=ce
# Sat, 12 Nov 2022 08:33:20 GMT
ENV ASSET=ce
# Sat, 12 Nov 2022 08:33:20 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 08:33:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 12 Nov 2022 08:33:20 GMT
ARG KONG_VERSION=2.8.3
# Sat, 12 Nov 2022 08:33:20 GMT
ENV KONG_VERSION=2.8.3
# Sat, 12 Nov 2022 08:33:20 GMT
ARG KONG_AMD64_SHA=962ac92c9834cb59f1d6563412714f3d6eecfe6c6849a84cfcbe7a4b3facbf46
# Sat, 12 Nov 2022 08:33:20 GMT
ARG KONG_ARM64_SHA=7076e6ee6a03df86795a1a08cf86e0349a150095e61be266db462cb7de9fd745
# Sat, 12 Nov 2022 08:33:27 GMT
# ARGS: KONG_AMD64_SHA=962ac92c9834cb59f1d6563412714f3d6eecfe6c6849a84cfcbe7a4b3facbf46 KONG_ARM64_SHA=7076e6ee6a03df86795a1a08cf86e0349a150095e61be266db462cb7de9fd745
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 12 Nov 2022 08:33:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 08:33:28 GMT
USER kong
# Sat, 12 Nov 2022 08:33:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:33:28 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 08:33:28 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 08:33:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 08:33:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb280baa9a48dcb41479263bee3784fcbf4fd49e55fb1ce556437aac0a14f66e`  
		Last Modified: Sat, 12 Nov 2022 08:34:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a483e5d82932b46ee26095c1122af40655ec240003f002ade98f3ef69ab4bcf`  
		Last Modified: Sat, 12 Nov 2022 08:34:50 GMT  
		Size: 46.5 MB (46528047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0809b8d4226790980e9e9596b9ebf2858c446e3db58b4f87d07ffe23495c750e`  
		Last Modified: Sat, 12 Nov 2022 08:34:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.3-alpine`

```console
$ docker pull kong@sha256:52ba05e86adcc19d7409c82840fee3773d84f3ff9f768832459af78914aeafb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:a8eb48a7e0b6a6231f4f44f8e0ec795dd322b44c7004dc00922862dad7d68199
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49335332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a4481ac0d615c6a0ae74e00fa1e67ac5efbe29eb4429e696bd6020f6fb919e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 12 Nov 2022 08:33:20 GMT
ARG ASSET=ce
# Sat, 12 Nov 2022 08:33:20 GMT
ENV ASSET=ce
# Sat, 12 Nov 2022 08:33:20 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 08:33:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 12 Nov 2022 08:33:20 GMT
ARG KONG_VERSION=2.8.3
# Sat, 12 Nov 2022 08:33:20 GMT
ENV KONG_VERSION=2.8.3
# Sat, 12 Nov 2022 08:33:20 GMT
ARG KONG_AMD64_SHA=962ac92c9834cb59f1d6563412714f3d6eecfe6c6849a84cfcbe7a4b3facbf46
# Sat, 12 Nov 2022 08:33:20 GMT
ARG KONG_ARM64_SHA=7076e6ee6a03df86795a1a08cf86e0349a150095e61be266db462cb7de9fd745
# Sat, 12 Nov 2022 08:33:27 GMT
# ARGS: KONG_AMD64_SHA=962ac92c9834cb59f1d6563412714f3d6eecfe6c6849a84cfcbe7a4b3facbf46 KONG_ARM64_SHA=7076e6ee6a03df86795a1a08cf86e0349a150095e61be266db462cb7de9fd745
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 12 Nov 2022 08:33:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 08:33:28 GMT
USER kong
# Sat, 12 Nov 2022 08:33:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:33:28 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 08:33:28 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 08:33:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 08:33:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb280baa9a48dcb41479263bee3784fcbf4fd49e55fb1ce556437aac0a14f66e`  
		Last Modified: Sat, 12 Nov 2022 08:34:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a483e5d82932b46ee26095c1122af40655ec240003f002ade98f3ef69ab4bcf`  
		Last Modified: Sat, 12 Nov 2022 08:34:50 GMT  
		Size: 46.5 MB (46528047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0809b8d4226790980e9e9596b9ebf2858c446e3db58b4f87d07ffe23495c750e`  
		Last Modified: Sat, 12 Nov 2022 08:34:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.3-ubuntu`

```console
$ docker pull kong@sha256:0468649d9729a6576c5122996c0ec7e5c64f01a8a10e38c3a0291f0e24587dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:027f3304be0620a44e95c313bbb2ec683f42fb0f077433e958fd8542cab49439
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119163850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f3625d05e9a144ab3a04ddc2827252120d95bb1c15ce093e45c2c190c0aa32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:20:29 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:20:29 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:20:29 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:20:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:20:30 GMT
ARG KONG_VERSION=2.8.3
# Fri, 09 Dec 2022 02:20:30 GMT
ENV KONG_VERSION=2.8.3
# Fri, 09 Dec 2022 02:20:30 GMT
ARG KONG_AMD64_SHA=897e159da8e1432e474794d1e25d81fe6548adfa7b68beb186365d732e031d63
# Fri, 09 Dec 2022 02:20:30 GMT
ARG KONG_ARM64_SHA=5f806a19dcb3f4f41108fd6472a2480c7f6032519ecb506de5c9da8a0faf8172
# Fri, 09 Dec 2022 02:20:58 GMT
# ARGS: KONG_AMD64_SHA=897e159da8e1432e474794d1e25d81fe6548adfa7b68beb186365d732e031d63 KONG_ARM64_SHA=5f806a19dcb3f4f41108fd6472a2480c7f6032519ecb506de5c9da8a0faf8172
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:20:58 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:20:58 GMT
USER kong
# Fri, 09 Dec 2022 02:20:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:20:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:20:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:20:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:20:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2474cb36d2a55205f237b1c32237602452e0ed8d89aef167678418cc2273d`  
		Last Modified: Fri, 09 Dec 2022 02:23:57 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c75b22921c0bbb0198757ae391953d69cff9bb88e2a1766b12b6d618bde261`  
		Last Modified: Fri, 09 Dec 2022 02:24:07 GMT  
		Size: 67.4 MB (67369548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c182791e4fe2c7484fa0448513d9d9bd02a5061dc761c0daf005b847b8f79f`  
		Last Modified: Fri, 09 Dec 2022 02:23:56 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3`

```console
$ docker pull kong@sha256:bb341351f2aa1a0ba207718b1990c63519c63c5cd2a1e5ab06b686dbcd2507e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:19fd008047b35ca8ac9911160484bf27a26cfe545271d7ab7705f6f7a3981456
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75684069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bef4e17bc7c60b36ec005874aa9e620c149f532e120989fccb1ee265af816d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 01:46:26 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 01:46:27 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 01:46:27 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 01:46:35 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 01:46:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 01:46:35 GMT
USER kong
# Wed, 07 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 01:46:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 01:46:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 01:46:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 01:46:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c20196a899ca5c3eff49961ea4317896637fb1280fe97fd49293204ea5003`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c20ec930ae07f14a3f033d60be441de2337f3d018bdabe202bf9285080fb1`  
		Last Modified: Wed, 07 Dec 2022 01:49:17 GMT  
		Size: 72.9 MB (72876782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1649aa893189861145c730ec634934ed5cf4a4bb6a0ed7dddfc65d4ead7430cd`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:320d7a3f1821d29a9f9844f072ebeddd913c23f13bb857255192556c3f7ef722
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73700301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f4d4009961866b1965309f7ab521ebba185c64f4f1615e6f0e6dbc03f0902`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 00:39:59 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 00:39:59 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 00:39:59 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 00:40:05 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 00:40:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 00:40:06 GMT
USER kong
# Wed, 07 Dec 2022 00:40:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 00:40:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 00:40:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 00:40:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 00:40:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f48f77bf41098f2f664023d59a50bc165e6f3059c57f2743f5cb916962eb043`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af513948f28e8bea3a5a4c61064f55f95feda819758f8238169d34a149301c9b`  
		Last Modified: Wed, 07 Dec 2022 00:44:55 GMT  
		Size: 71.0 MB (70991528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6f63eb31c7aa20531d430db31d5834e6b8c487230c27804a70b8df638b49f6`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0`

```console
$ docker pull kong@sha256:9f5b00c723e2436d82cdb3c7440bdac452cfae1483986b8fb9928ba7538c38f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0` - linux; amd64

```console
$ docker pull kong@sha256:45afa102dbc7470fe7a4f741bd9b62cb283fb45941a5a8fac3e33f6c7933a142
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75538377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a3215492d0cc352dc365b634a6559e6830af41c950eb520b60d3d1f0861ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 08:33:04 GMT
ENV KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Sat, 12 Nov 2022 08:33:04 GMT
ARG ASSET=remote
# Sat, 12 Nov 2022 08:33:04 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 08:33:05 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 12 Nov 2022 08:33:13 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 12 Nov 2022 08:33:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 08:33:14 GMT
USER kong
# Sat, 12 Nov 2022 08:33:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:33:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 08:33:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 08:33:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 08:33:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06284b2d3acb73bd2b35d03f2e96c0c17b6d3026717bdf7aba9dad83a0493a4b`  
		Last Modified: Sat, 12 Nov 2022 08:34:12 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d35029cb6a1ad317d616333c17ba075563a952fcfcedfb58303690a71cf2510`  
		Last Modified: Sat, 12 Nov 2022 08:34:21 GMT  
		Size: 72.7 MB (72731096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e890f886f3ad09dce2c89c9e477a1e73f50d83cd563400484e6c09904f93799c`  
		Last Modified: Sat, 12 Nov 2022 08:34:12 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:25b187fcd9ecac9db05adabe438d68d09d430854241f54fbd4849a19f6f90f4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73537168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ce94b18c8a72fedb2b055cbbc84e2c6b84f8204f4086efcd65921826786b8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 12 Nov 2022 04:27:43 GMT
ARG KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:43 GMT
ENV KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Sat, 12 Nov 2022 04:27:44 GMT
ARG ASSET=remote
# Sat, 12 Nov 2022 04:27:44 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 04:27:44 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 12 Nov 2022 04:27:51 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 12 Nov 2022 04:27:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 04:27:52 GMT
USER kong
# Sat, 12 Nov 2022 04:27:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:27:52 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 04:27:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 04:27:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 04:27:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e04f8e193571681898f535d00719ae347a2ee8873a72a6520167dc9c128091`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad12cb9acc717d4960140d35382d1f782ce2e51aacc2f6ad3101bc6106db6c5`  
		Last Modified: Sat, 12 Nov 2022 04:30:21 GMT  
		Size: 70.8 MB (70828396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276145d452351533920e24f4a22aca2f2d76f8ebbca1bef83b44ca5578386672`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0-alpine`

```console
$ docker pull kong@sha256:9f5b00c723e2436d82cdb3c7440bdac452cfae1483986b8fb9928ba7538c38f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:45afa102dbc7470fe7a4f741bd9b62cb283fb45941a5a8fac3e33f6c7933a142
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75538377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a3215492d0cc352dc365b634a6559e6830af41c950eb520b60d3d1f0861ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 08:33:04 GMT
ENV KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Sat, 12 Nov 2022 08:33:04 GMT
ARG ASSET=remote
# Sat, 12 Nov 2022 08:33:04 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 08:33:05 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 12 Nov 2022 08:33:13 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 12 Nov 2022 08:33:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 08:33:14 GMT
USER kong
# Sat, 12 Nov 2022 08:33:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:33:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 08:33:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 08:33:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 08:33:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06284b2d3acb73bd2b35d03f2e96c0c17b6d3026717bdf7aba9dad83a0493a4b`  
		Last Modified: Sat, 12 Nov 2022 08:34:12 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d35029cb6a1ad317d616333c17ba075563a952fcfcedfb58303690a71cf2510`  
		Last Modified: Sat, 12 Nov 2022 08:34:21 GMT  
		Size: 72.7 MB (72731096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e890f886f3ad09dce2c89c9e477a1e73f50d83cd563400484e6c09904f93799c`  
		Last Modified: Sat, 12 Nov 2022 08:34:12 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:25b187fcd9ecac9db05adabe438d68d09d430854241f54fbd4849a19f6f90f4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73537168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ce94b18c8a72fedb2b055cbbc84e2c6b84f8204f4086efcd65921826786b8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 12 Nov 2022 04:27:43 GMT
ARG KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:43 GMT
ENV KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Sat, 12 Nov 2022 04:27:44 GMT
ARG ASSET=remote
# Sat, 12 Nov 2022 04:27:44 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 04:27:44 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 12 Nov 2022 04:27:51 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 12 Nov 2022 04:27:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 04:27:52 GMT
USER kong
# Sat, 12 Nov 2022 04:27:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:27:52 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 04:27:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 04:27:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 04:27:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e04f8e193571681898f535d00719ae347a2ee8873a72a6520167dc9c128091`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad12cb9acc717d4960140d35382d1f782ce2e51aacc2f6ad3101bc6106db6c5`  
		Last Modified: Sat, 12 Nov 2022 04:30:21 GMT  
		Size: 70.8 MB (70828396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276145d452351533920e24f4a22aca2f2d76f8ebbca1bef83b44ca5578386672`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0-ubuntu`

```console
$ docker pull kong@sha256:71c803a17a20c87c6b04952d4044be1ba18c32c7f0f51e859e71249e2d8bbfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c84757f21a8c48e9ecda2deb9ce2adb904c3ba0c09a9bae27e0c26897afbb217
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101683366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae95e84cbb1a0e700275727a3cf929f34ba7f132f459c59c52884a65fb933cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:19:23 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 02:19:23 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:19:23 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:19:59 GMT
ARG KONG_VERSION=3.0.1
# Fri, 09 Dec 2022 02:19:59 GMT
ENV KONG_VERSION=3.0.1
# Fri, 09 Dec 2022 02:19:59 GMT
ARG KONG_AMD64_SHA=36f05448b4bba55cfaccddb30a376c952b5be850892af2ca1be904001ebb446a
# Fri, 09 Dec 2022 02:19:59 GMT
ARG KONG_ARM64_SHA=309aab0262f7b835035975b98c62af98bf4469c7596a03d7d73195f480a49e89
# Fri, 09 Dec 2022 02:20:21 GMT
# ARGS: KONG_AMD64_SHA=36f05448b4bba55cfaccddb30a376c952b5be850892af2ca1be904001ebb446a KONG_ARM64_SHA=309aab0262f7b835035975b98c62af98bf4469c7596a03d7d73195f480a49e89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:20:22 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:20:22 GMT
USER kong
# Fri, 09 Dec 2022 02:20:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:20:22 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:20:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:20:22 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:20:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d7c9b92669dc7ad55e9d4346f9833d39acca1c6659122b6ffc3e7e59e42abb`  
		Last Modified: Fri, 09 Dec 2022 02:23:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6bf1b287be31c08a07fd18a4270dd99adab6a2784ae9e185da4a245970d94`  
		Last Modified: Fri, 09 Dec 2022 02:23:45 GMT  
		Size: 73.1 MB (73105474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce50da9902c8a8f36adc946c37ec2f98ca41e94f3f9576dd83598cac7744d9d7`  
		Last Modified: Fri, 09 Dec 2022 02:23:33 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:551053d41a8a8f9c7ceaf3f0799499379c96b6210ea1158389cde2decbc524a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98934952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5c6288deb6d964a50067423ab9c72a21791e2c0a81958fac63109e61b61cd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:44:14 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 04:44:14 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:44:15 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:44:57 GMT
ARG KONG_VERSION=3.0.1
# Fri, 09 Dec 2022 04:44:57 GMT
ENV KONG_VERSION=3.0.1
# Fri, 09 Dec 2022 04:44:57 GMT
ARG KONG_AMD64_SHA=36f05448b4bba55cfaccddb30a376c952b5be850892af2ca1be904001ebb446a
# Fri, 09 Dec 2022 04:44:57 GMT
ARG KONG_ARM64_SHA=309aab0262f7b835035975b98c62af98bf4469c7596a03d7d73195f480a49e89
# Fri, 09 Dec 2022 04:45:13 GMT
# ARGS: KONG_AMD64_SHA=36f05448b4bba55cfaccddb30a376c952b5be850892af2ca1be904001ebb446a KONG_ARM64_SHA=309aab0262f7b835035975b98c62af98bf4469c7596a03d7d73195f480a49e89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:45:14 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:45:14 GMT
USER kong
# Fri, 09 Dec 2022 04:45:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:45:14 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:45:14 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:45:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:45:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359a97e76580b42bec113a53e79fada5dda3b02cba5dd58e05cb2c6efae5d23a`  
		Last Modified: Fri, 09 Dec 2022 04:48:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8737ac239fbab4fbcf30c52cee64a5ce86bb6eb8564f091d0e6ce1e16cd6006`  
		Last Modified: Fri, 09 Dec 2022 04:49:00 GMT  
		Size: 71.7 MB (71740774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7308033d187f59e984efd74cc8df8619deebaf97a7d109e3cc66709c2d1cfdcf`  
		Last Modified: Fri, 09 Dec 2022 04:48:51 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.1`

```console
$ docker pull kong@sha256:9f5b00c723e2436d82cdb3c7440bdac452cfae1483986b8fb9928ba7538c38f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.1` - linux; amd64

```console
$ docker pull kong@sha256:45afa102dbc7470fe7a4f741bd9b62cb283fb45941a5a8fac3e33f6c7933a142
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75538377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a3215492d0cc352dc365b634a6559e6830af41c950eb520b60d3d1f0861ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 08:33:04 GMT
ENV KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Sat, 12 Nov 2022 08:33:04 GMT
ARG ASSET=remote
# Sat, 12 Nov 2022 08:33:04 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 08:33:05 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 12 Nov 2022 08:33:13 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 12 Nov 2022 08:33:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 08:33:14 GMT
USER kong
# Sat, 12 Nov 2022 08:33:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:33:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 08:33:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 08:33:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 08:33:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06284b2d3acb73bd2b35d03f2e96c0c17b6d3026717bdf7aba9dad83a0493a4b`  
		Last Modified: Sat, 12 Nov 2022 08:34:12 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d35029cb6a1ad317d616333c17ba075563a952fcfcedfb58303690a71cf2510`  
		Last Modified: Sat, 12 Nov 2022 08:34:21 GMT  
		Size: 72.7 MB (72731096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e890f886f3ad09dce2c89c9e477a1e73f50d83cd563400484e6c09904f93799c`  
		Last Modified: Sat, 12 Nov 2022 08:34:12 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:25b187fcd9ecac9db05adabe438d68d09d430854241f54fbd4849a19f6f90f4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73537168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ce94b18c8a72fedb2b055cbbc84e2c6b84f8204f4086efcd65921826786b8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 12 Nov 2022 04:27:43 GMT
ARG KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:43 GMT
ENV KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Sat, 12 Nov 2022 04:27:44 GMT
ARG ASSET=remote
# Sat, 12 Nov 2022 04:27:44 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 04:27:44 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 12 Nov 2022 04:27:51 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 12 Nov 2022 04:27:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 04:27:52 GMT
USER kong
# Sat, 12 Nov 2022 04:27:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:27:52 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 04:27:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 04:27:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 04:27:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e04f8e193571681898f535d00719ae347a2ee8873a72a6520167dc9c128091`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad12cb9acc717d4960140d35382d1f782ce2e51aacc2f6ad3101bc6106db6c5`  
		Last Modified: Sat, 12 Nov 2022 04:30:21 GMT  
		Size: 70.8 MB (70828396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276145d452351533920e24f4a22aca2f2d76f8ebbca1bef83b44ca5578386672`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.1-alpine`

```console
$ docker pull kong@sha256:9f5b00c723e2436d82cdb3c7440bdac452cfae1483986b8fb9928ba7538c38f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:45afa102dbc7470fe7a4f741bd9b62cb283fb45941a5a8fac3e33f6c7933a142
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75538377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a3215492d0cc352dc365b634a6559e6830af41c950eb520b60d3d1f0861ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 08:33:04 GMT
ENV KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Sat, 12 Nov 2022 08:33:04 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Sat, 12 Nov 2022 08:33:04 GMT
ARG ASSET=remote
# Sat, 12 Nov 2022 08:33:04 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 08:33:05 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 12 Nov 2022 08:33:13 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 12 Nov 2022 08:33:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 08:33:14 GMT
USER kong
# Sat, 12 Nov 2022 08:33:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:33:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 08:33:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 08:33:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 08:33:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06284b2d3acb73bd2b35d03f2e96c0c17b6d3026717bdf7aba9dad83a0493a4b`  
		Last Modified: Sat, 12 Nov 2022 08:34:12 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d35029cb6a1ad317d616333c17ba075563a952fcfcedfb58303690a71cf2510`  
		Last Modified: Sat, 12 Nov 2022 08:34:21 GMT  
		Size: 72.7 MB (72731096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e890f886f3ad09dce2c89c9e477a1e73f50d83cd563400484e6c09904f93799c`  
		Last Modified: Sat, 12 Nov 2022 08:34:12 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:25b187fcd9ecac9db05adabe438d68d09d430854241f54fbd4849a19f6f90f4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73537168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ce94b18c8a72fedb2b055cbbc84e2c6b84f8204f4086efcd65921826786b8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 12 Nov 2022 04:27:43 GMT
ARG KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:43 GMT
ENV KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Sat, 12 Nov 2022 04:27:44 GMT
ARG ASSET=remote
# Sat, 12 Nov 2022 04:27:44 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 04:27:44 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 12 Nov 2022 04:27:51 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 12 Nov 2022 04:27:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 04:27:52 GMT
USER kong
# Sat, 12 Nov 2022 04:27:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:27:52 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 04:27:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 04:27:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 04:27:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e04f8e193571681898f535d00719ae347a2ee8873a72a6520167dc9c128091`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad12cb9acc717d4960140d35382d1f782ce2e51aacc2f6ad3101bc6106db6c5`  
		Last Modified: Sat, 12 Nov 2022 04:30:21 GMT  
		Size: 70.8 MB (70828396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276145d452351533920e24f4a22aca2f2d76f8ebbca1bef83b44ca5578386672`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.1-ubuntu`

```console
$ docker pull kong@sha256:71c803a17a20c87c6b04952d4044be1ba18c32c7f0f51e859e71249e2d8bbfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c84757f21a8c48e9ecda2deb9ce2adb904c3ba0c09a9bae27e0c26897afbb217
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101683366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae95e84cbb1a0e700275727a3cf929f34ba7f132f459c59c52884a65fb933cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:19:23 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 02:19:23 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:19:23 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:19:59 GMT
ARG KONG_VERSION=3.0.1
# Fri, 09 Dec 2022 02:19:59 GMT
ENV KONG_VERSION=3.0.1
# Fri, 09 Dec 2022 02:19:59 GMT
ARG KONG_AMD64_SHA=36f05448b4bba55cfaccddb30a376c952b5be850892af2ca1be904001ebb446a
# Fri, 09 Dec 2022 02:19:59 GMT
ARG KONG_ARM64_SHA=309aab0262f7b835035975b98c62af98bf4469c7596a03d7d73195f480a49e89
# Fri, 09 Dec 2022 02:20:21 GMT
# ARGS: KONG_AMD64_SHA=36f05448b4bba55cfaccddb30a376c952b5be850892af2ca1be904001ebb446a KONG_ARM64_SHA=309aab0262f7b835035975b98c62af98bf4469c7596a03d7d73195f480a49e89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:20:22 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:20:22 GMT
USER kong
# Fri, 09 Dec 2022 02:20:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:20:22 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:20:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:20:22 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:20:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d7c9b92669dc7ad55e9d4346f9833d39acca1c6659122b6ffc3e7e59e42abb`  
		Last Modified: Fri, 09 Dec 2022 02:23:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6bf1b287be31c08a07fd18a4270dd99adab6a2784ae9e185da4a245970d94`  
		Last Modified: Fri, 09 Dec 2022 02:23:45 GMT  
		Size: 73.1 MB (73105474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce50da9902c8a8f36adc946c37ec2f98ca41e94f3f9576dd83598cac7744d9d7`  
		Last Modified: Fri, 09 Dec 2022 02:23:33 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:551053d41a8a8f9c7ceaf3f0799499379c96b6210ea1158389cde2decbc524a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98934952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5c6288deb6d964a50067423ab9c72a21791e2c0a81958fac63109e61b61cd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:44:14 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 04:44:14 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:44:15 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:44:57 GMT
ARG KONG_VERSION=3.0.1
# Fri, 09 Dec 2022 04:44:57 GMT
ENV KONG_VERSION=3.0.1
# Fri, 09 Dec 2022 04:44:57 GMT
ARG KONG_AMD64_SHA=36f05448b4bba55cfaccddb30a376c952b5be850892af2ca1be904001ebb446a
# Fri, 09 Dec 2022 04:44:57 GMT
ARG KONG_ARM64_SHA=309aab0262f7b835035975b98c62af98bf4469c7596a03d7d73195f480a49e89
# Fri, 09 Dec 2022 04:45:13 GMT
# ARGS: KONG_AMD64_SHA=36f05448b4bba55cfaccddb30a376c952b5be850892af2ca1be904001ebb446a KONG_ARM64_SHA=309aab0262f7b835035975b98c62af98bf4469c7596a03d7d73195f480a49e89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:45:14 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:45:14 GMT
USER kong
# Fri, 09 Dec 2022 04:45:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:45:14 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:45:14 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:45:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:45:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359a97e76580b42bec113a53e79fada5dda3b02cba5dd58e05cb2c6efae5d23a`  
		Last Modified: Fri, 09 Dec 2022 04:48:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8737ac239fbab4fbcf30c52cee64a5ce86bb6eb8564f091d0e6ce1e16cd6006`  
		Last Modified: Fri, 09 Dec 2022 04:49:00 GMT  
		Size: 71.7 MB (71740774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7308033d187f59e984efd74cc8df8619deebaf97a7d109e3cc66709c2d1cfdcf`  
		Last Modified: Fri, 09 Dec 2022 04:48:51 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1`

```console
$ docker pull kong@sha256:bb341351f2aa1a0ba207718b1990c63519c63c5cd2a1e5ab06b686dbcd2507e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1` - linux; amd64

```console
$ docker pull kong@sha256:19fd008047b35ca8ac9911160484bf27a26cfe545271d7ab7705f6f7a3981456
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75684069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bef4e17bc7c60b36ec005874aa9e620c149f532e120989fccb1ee265af816d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 01:46:26 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 01:46:27 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 01:46:27 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 01:46:35 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 01:46:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 01:46:35 GMT
USER kong
# Wed, 07 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 01:46:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 01:46:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 01:46:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 01:46:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c20196a899ca5c3eff49961ea4317896637fb1280fe97fd49293204ea5003`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c20ec930ae07f14a3f033d60be441de2337f3d018bdabe202bf9285080fb1`  
		Last Modified: Wed, 07 Dec 2022 01:49:17 GMT  
		Size: 72.9 MB (72876782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1649aa893189861145c730ec634934ed5cf4a4bb6a0ed7dddfc65d4ead7430cd`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:320d7a3f1821d29a9f9844f072ebeddd913c23f13bb857255192556c3f7ef722
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73700301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f4d4009961866b1965309f7ab521ebba185c64f4f1615e6f0e6dbc03f0902`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 00:39:59 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 00:39:59 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 00:39:59 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 00:40:05 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 00:40:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 00:40:06 GMT
USER kong
# Wed, 07 Dec 2022 00:40:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 00:40:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 00:40:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 00:40:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 00:40:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f48f77bf41098f2f664023d59a50bc165e6f3059c57f2743f5cb916962eb043`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af513948f28e8bea3a5a4c61064f55f95feda819758f8238169d34a149301c9b`  
		Last Modified: Wed, 07 Dec 2022 00:44:55 GMT  
		Size: 71.0 MB (70991528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6f63eb31c7aa20531d430db31d5834e6b8c487230c27804a70b8df638b49f6`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1-ubuntu`

```console
$ docker pull kong@sha256:b2b34db750839d5a2994196037d341dd06011f07da7732cd57ab57629d9fc1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6622b4957485ed546ce795f7914c7ecfd1ebd5b37d540d0714fd257793433bd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101721258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c3363408922c7c710be22906c1126376f87da071e321f35b815d030092b70e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:19:23 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 02:19:23 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:19:23 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:19:23 GMT
ARG KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 02:19:23 GMT
ENV KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 02:19:23 GMT
ARG KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b
# Fri, 09 Dec 2022 02:19:24 GMT
ARG KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
# Fri, 09 Dec 2022 02:19:52 GMT
# ARGS: KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:19:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:19:53 GMT
USER kong
# Fri, 09 Dec 2022 02:19:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:19:53 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:19:53 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:19:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:19:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d7c9b92669dc7ad55e9d4346f9833d39acca1c6659122b6ffc3e7e59e42abb`  
		Last Modified: Fri, 09 Dec 2022 02:23:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fa518cc6bbaee07dfa3ae158b5a67a769592ddf5872e3d703296583e4a7481`  
		Last Modified: Fri, 09 Dec 2022 02:23:21 GMT  
		Size: 73.1 MB (73143366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb8a94e4041fdeb1780e284d0f48cd7e2e6a5294ed9548d596c54343eaae09`  
		Last Modified: Fri, 09 Dec 2022 02:23:09 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:da346463291c9aeee47fb865337bf9c1e8b7931529a81920021015b40f6c3629
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98954332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3576028316872bcdbd5e6c6c5e81a3e701439202a4fbc3cd9400efc765d0623`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:44:14 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 04:44:14 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:44:15 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:44:15 GMT
ARG KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 04:44:15 GMT
ENV KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 04:44:15 GMT
ARG KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b
# Fri, 09 Dec 2022 04:44:15 GMT
ARG KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
# Fri, 09 Dec 2022 04:44:46 GMT
# ARGS: KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:44:48 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:44:48 GMT
USER kong
# Fri, 09 Dec 2022 04:44:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:44:48 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:44:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:44:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:44:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359a97e76580b42bec113a53e79fada5dda3b02cba5dd58e05cb2c6efae5d23a`  
		Last Modified: Fri, 09 Dec 2022 04:48:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7bdf8f709625b9291d491eda77dd4cd5f7ca0b5cc181fdd3594c1bb1cd8979`  
		Last Modified: Fri, 09 Dec 2022 04:48:39 GMT  
		Size: 71.8 MB (71760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee280144483d82b9cd6f14a962b1013f6bd817dd25fabd001e277297cb68e075`  
		Last Modified: Fri, 09 Dec 2022 04:48:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.0`

```console
$ docker pull kong@sha256:bb341351f2aa1a0ba207718b1990c63519c63c5cd2a1e5ab06b686dbcd2507e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.0` - linux; amd64

```console
$ docker pull kong@sha256:19fd008047b35ca8ac9911160484bf27a26cfe545271d7ab7705f6f7a3981456
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75684069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bef4e17bc7c60b36ec005874aa9e620c149f532e120989fccb1ee265af816d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 01:46:26 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 01:46:27 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 01:46:27 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 01:46:35 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 01:46:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 01:46:35 GMT
USER kong
# Wed, 07 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 01:46:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 01:46:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 01:46:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 01:46:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c20196a899ca5c3eff49961ea4317896637fb1280fe97fd49293204ea5003`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c20ec930ae07f14a3f033d60be441de2337f3d018bdabe202bf9285080fb1`  
		Last Modified: Wed, 07 Dec 2022 01:49:17 GMT  
		Size: 72.9 MB (72876782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1649aa893189861145c730ec634934ed5cf4a4bb6a0ed7dddfc65d4ead7430cd`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:320d7a3f1821d29a9f9844f072ebeddd913c23f13bb857255192556c3f7ef722
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73700301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f4d4009961866b1965309f7ab521ebba185c64f4f1615e6f0e6dbc03f0902`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 00:39:59 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 00:39:59 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 00:39:59 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 00:40:05 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 00:40:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 00:40:06 GMT
USER kong
# Wed, 07 Dec 2022 00:40:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 00:40:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 00:40:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 00:40:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 00:40:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f48f77bf41098f2f664023d59a50bc165e6f3059c57f2743f5cb916962eb043`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af513948f28e8bea3a5a4c61064f55f95feda819758f8238169d34a149301c9b`  
		Last Modified: Wed, 07 Dec 2022 00:44:55 GMT  
		Size: 71.0 MB (70991528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6f63eb31c7aa20531d430db31d5834e6b8c487230c27804a70b8df638b49f6`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.0-alpine`

```console
$ docker pull kong@sha256:bb341351f2aa1a0ba207718b1990c63519c63c5cd2a1e5ab06b686dbcd2507e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:19fd008047b35ca8ac9911160484bf27a26cfe545271d7ab7705f6f7a3981456
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75684069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bef4e17bc7c60b36ec005874aa9e620c149f532e120989fccb1ee265af816d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 01:46:26 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 01:46:27 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 01:46:27 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 01:46:35 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 01:46:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 01:46:35 GMT
USER kong
# Wed, 07 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 01:46:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 01:46:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 01:46:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 01:46:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c20196a899ca5c3eff49961ea4317896637fb1280fe97fd49293204ea5003`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c20ec930ae07f14a3f033d60be441de2337f3d018bdabe202bf9285080fb1`  
		Last Modified: Wed, 07 Dec 2022 01:49:17 GMT  
		Size: 72.9 MB (72876782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1649aa893189861145c730ec634934ed5cf4a4bb6a0ed7dddfc65d4ead7430cd`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:320d7a3f1821d29a9f9844f072ebeddd913c23f13bb857255192556c3f7ef722
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73700301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f4d4009961866b1965309f7ab521ebba185c64f4f1615e6f0e6dbc03f0902`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 00:39:59 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 00:39:59 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 00:39:59 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 00:40:05 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 00:40:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 00:40:06 GMT
USER kong
# Wed, 07 Dec 2022 00:40:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 00:40:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 00:40:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 00:40:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 00:40:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f48f77bf41098f2f664023d59a50bc165e6f3059c57f2743f5cb916962eb043`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af513948f28e8bea3a5a4c61064f55f95feda819758f8238169d34a149301c9b`  
		Last Modified: Wed, 07 Dec 2022 00:44:55 GMT  
		Size: 71.0 MB (70991528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6f63eb31c7aa20531d430db31d5834e6b8c487230c27804a70b8df638b49f6`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.0-ubuntu`

```console
$ docker pull kong@sha256:b2b34db750839d5a2994196037d341dd06011f07da7732cd57ab57629d9fc1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6622b4957485ed546ce795f7914c7ecfd1ebd5b37d540d0714fd257793433bd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101721258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c3363408922c7c710be22906c1126376f87da071e321f35b815d030092b70e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:19:23 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 02:19:23 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:19:23 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:19:23 GMT
ARG KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 02:19:23 GMT
ENV KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 02:19:23 GMT
ARG KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b
# Fri, 09 Dec 2022 02:19:24 GMT
ARG KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
# Fri, 09 Dec 2022 02:19:52 GMT
# ARGS: KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:19:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:19:53 GMT
USER kong
# Fri, 09 Dec 2022 02:19:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:19:53 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:19:53 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:19:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:19:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d7c9b92669dc7ad55e9d4346f9833d39acca1c6659122b6ffc3e7e59e42abb`  
		Last Modified: Fri, 09 Dec 2022 02:23:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fa518cc6bbaee07dfa3ae158b5a67a769592ddf5872e3d703296583e4a7481`  
		Last Modified: Fri, 09 Dec 2022 02:23:21 GMT  
		Size: 73.1 MB (73143366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb8a94e4041fdeb1780e284d0f48cd7e2e6a5294ed9548d596c54343eaae09`  
		Last Modified: Fri, 09 Dec 2022 02:23:09 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:da346463291c9aeee47fb865337bf9c1e8b7931529a81920021015b40f6c3629
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98954332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3576028316872bcdbd5e6c6c5e81a3e701439202a4fbc3cd9400efc765d0623`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:44:14 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 04:44:14 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:44:15 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:44:15 GMT
ARG KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 04:44:15 GMT
ENV KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 04:44:15 GMT
ARG KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b
# Fri, 09 Dec 2022 04:44:15 GMT
ARG KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
# Fri, 09 Dec 2022 04:44:46 GMT
# ARGS: KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:44:48 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:44:48 GMT
USER kong
# Fri, 09 Dec 2022 04:44:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:44:48 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:44:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:44:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:44:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359a97e76580b42bec113a53e79fada5dda3b02cba5dd58e05cb2c6efae5d23a`  
		Last Modified: Fri, 09 Dec 2022 04:48:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7bdf8f709625b9291d491eda77dd4cd5f7ca0b5cc181fdd3594c1bb1cd8979`  
		Last Modified: Fri, 09 Dec 2022 04:48:39 GMT  
		Size: 71.8 MB (71760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee280144483d82b9cd6f14a962b1013f6bd817dd25fabd001e277297cb68e075`  
		Last Modified: Fri, 09 Dec 2022 04:48:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:bb341351f2aa1a0ba207718b1990c63519c63c5cd2a1e5ab06b686dbcd2507e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:19fd008047b35ca8ac9911160484bf27a26cfe545271d7ab7705f6f7a3981456
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75684069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bef4e17bc7c60b36ec005874aa9e620c149f532e120989fccb1ee265af816d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 01:46:26 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 01:46:27 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 01:46:27 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 01:46:35 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 01:46:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 01:46:35 GMT
USER kong
# Wed, 07 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 01:46:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 01:46:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 01:46:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 01:46:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c20196a899ca5c3eff49961ea4317896637fb1280fe97fd49293204ea5003`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c20ec930ae07f14a3f033d60be441de2337f3d018bdabe202bf9285080fb1`  
		Last Modified: Wed, 07 Dec 2022 01:49:17 GMT  
		Size: 72.9 MB (72876782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1649aa893189861145c730ec634934ed5cf4a4bb6a0ed7dddfc65d4ead7430cd`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:320d7a3f1821d29a9f9844f072ebeddd913c23f13bb857255192556c3f7ef722
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73700301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f4d4009961866b1965309f7ab521ebba185c64f4f1615e6f0e6dbc03f0902`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 00:39:59 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 00:39:59 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 00:39:59 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 00:40:05 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 00:40:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 00:40:06 GMT
USER kong
# Wed, 07 Dec 2022 00:40:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 00:40:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 00:40:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 00:40:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 00:40:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f48f77bf41098f2f664023d59a50bc165e6f3059c57f2743f5cb916962eb043`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af513948f28e8bea3a5a4c61064f55f95feda819758f8238169d34a149301c9b`  
		Last Modified: Wed, 07 Dec 2022 00:44:55 GMT  
		Size: 71.0 MB (70991528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6f63eb31c7aa20531d430db31d5834e6b8c487230c27804a70b8df638b49f6`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:bb341351f2aa1a0ba207718b1990c63519c63c5cd2a1e5ab06b686dbcd2507e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:19fd008047b35ca8ac9911160484bf27a26cfe545271d7ab7705f6f7a3981456
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75684069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bef4e17bc7c60b36ec005874aa9e620c149f532e120989fccb1ee265af816d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:33:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 01:46:26 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 01:46:26 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 01:46:27 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 01:46:27 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 01:46:35 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 01:46:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 01:46:35 GMT
USER kong
# Wed, 07 Dec 2022 01:46:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 01:46:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 01:46:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 01:46:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 01:46:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373c20196a899ca5c3eff49961ea4317896637fb1280fe97fd49293204ea5003`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c20ec930ae07f14a3f033d60be441de2337f3d018bdabe202bf9285080fb1`  
		Last Modified: Wed, 07 Dec 2022 01:49:17 GMT  
		Size: 72.9 MB (72876782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1649aa893189861145c730ec634934ed5cf4a4bb6a0ed7dddfc65d4ead7430cd`  
		Last Modified: Wed, 07 Dec 2022 01:49:09 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:320d7a3f1821d29a9f9844f072ebeddd913c23f13bb857255192556c3f7ef722
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73700301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f4d4009961866b1965309f7ab521ebba185c64f4f1615e6f0e6dbc03f0902`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ENV KONG_VERSION=3.1.0
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6
# Wed, 07 Dec 2022 00:39:59 GMT
ARG KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
# Wed, 07 Dec 2022 00:39:59 GMT
ARG ASSET=remote
# Wed, 07 Dec 2022 00:39:59 GMT
ARG EE_PORTS
# Wed, 07 Dec 2022 00:39:59 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Wed, 07 Dec 2022 00:40:05 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bb302fede6a3081db998e1a6256f9def86f3ea31527888d08b745ff2dbc96f6 KONG_ARM64_SHA=001e1be3f8fec9bf50b9313a661ab3f97e1ececcb6debeac50b04adbc346983c
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Wed, 07 Dec 2022 00:40:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 07 Dec 2022 00:40:06 GMT
USER kong
# Wed, 07 Dec 2022 00:40:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Dec 2022 00:40:06 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 07 Dec 2022 00:40:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 07 Dec 2022 00:40:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 07 Dec 2022 00:40:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f48f77bf41098f2f664023d59a50bc165e6f3059c57f2743f5cb916962eb043`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af513948f28e8bea3a5a4c61064f55f95feda819758f8238169d34a149301c9b`  
		Last Modified: Wed, 07 Dec 2022 00:44:55 GMT  
		Size: 71.0 MB (70991528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6f63eb31c7aa20531d430db31d5834e6b8c487230c27804a70b8df638b49f6`  
		Last Modified: Wed, 07 Dec 2022 00:44:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:b2b34db750839d5a2994196037d341dd06011f07da7732cd57ab57629d9fc1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6622b4957485ed546ce795f7914c7ecfd1ebd5b37d540d0714fd257793433bd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101721258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c3363408922c7c710be22906c1126376f87da071e321f35b815d030092b70e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:19:23 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 02:19:23 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 02:19:23 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 02:19:23 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 02:19:23 GMT
ARG KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 02:19:23 GMT
ENV KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 02:19:23 GMT
ARG KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b
# Fri, 09 Dec 2022 02:19:24 GMT
ARG KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
# Fri, 09 Dec 2022 02:19:52 GMT
# ARGS: KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 02:19:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 02:19:53 GMT
USER kong
# Fri, 09 Dec 2022 02:19:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 02:19:53 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 02:19:53 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 02:19:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 02:19:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d7c9b92669dc7ad55e9d4346f9833d39acca1c6659122b6ffc3e7e59e42abb`  
		Last Modified: Fri, 09 Dec 2022 02:23:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fa518cc6bbaee07dfa3ae158b5a67a769592ddf5872e3d703296583e4a7481`  
		Last Modified: Fri, 09 Dec 2022 02:23:21 GMT  
		Size: 73.1 MB (73143366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb8a94e4041fdeb1780e284d0f48cd7e2e6a5294ed9548d596c54343eaae09`  
		Last Modified: Fri, 09 Dec 2022 02:23:09 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:da346463291c9aeee47fb865337bf9c1e8b7931529a81920021015b40f6c3629
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98954332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3576028316872bcdbd5e6c6c5e81a3e701439202a4fbc3cd9400efc765d0623`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:44:14 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 09 Dec 2022 04:44:14 GMT
ARG ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ENV ASSET=ce
# Fri, 09 Dec 2022 04:44:15 GMT
ARG EE_PORTS
# Fri, 09 Dec 2022 04:44:15 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 09 Dec 2022 04:44:15 GMT
ARG KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 04:44:15 GMT
ENV KONG_VERSION=3.1.0
# Fri, 09 Dec 2022 04:44:15 GMT
ARG KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b
# Fri, 09 Dec 2022 04:44:15 GMT
ARG KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
# Fri, 09 Dec 2022 04:44:46 GMT
# ARGS: KONG_AMD64_SHA=71f4c88a8319b35e264fbbd54dbdc5dd139369034b57bd0bdac789a08019974b KONG_ARM64_SHA=ff2f7b5d0dc3bd97e08fe4254400daf8a7d23f6ef2e72d9cec7c14e64bbc38b3
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 09 Dec 2022 04:44:48 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 09 Dec 2022 04:44:48 GMT
USER kong
# Fri, 09 Dec 2022 04:44:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:44:48 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 09 Dec 2022 04:44:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Dec 2022 04:44:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 09 Dec 2022 04:44:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359a97e76580b42bec113a53e79fada5dda3b02cba5dd58e05cb2c6efae5d23a`  
		Last Modified: Fri, 09 Dec 2022 04:48:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7bdf8f709625b9291d491eda77dd4cd5f7ca0b5cc181fdd3594c1bb1cd8979`  
		Last Modified: Fri, 09 Dec 2022 04:48:39 GMT  
		Size: 71.8 MB (71760152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee280144483d82b9cd6f14a962b1013f6bd817dd25fabd001e277297cb68e075`  
		Last Modified: Fri, 09 Dec 2022 04:48:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
