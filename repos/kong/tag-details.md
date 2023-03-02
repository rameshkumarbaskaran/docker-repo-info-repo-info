<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.3`](#kong283)
-	[`kong:2.8.3-alpine`](#kong283-alpine)
-	[`kong:2.8.3-ubuntu`](#kong283-ubuntu)
-	[`kong:3`](#kong3)
-	[`kong:3.0`](#kong30)
-	[`kong:3.0-alpine`](#kong30-alpine)
-	[`kong:3.0-ubuntu`](#kong30-ubuntu)
-	[`kong:3.0.2`](#kong302)
-	[`kong:3.0.2-alpine`](#kong302-alpine)
-	[`kong:3.0.2-ubuntu`](#kong302-ubuntu)
-	[`kong:3.1`](#kong31)
-	[`kong:3.1-ubuntu`](#kong31-ubuntu)
-	[`kong:3.1.1`](#kong311)
-	[`kong:3.1.1-alpine`](#kong311-alpine)
-	[`kong:3.1.1-ubuntu`](#kong311-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.8`

```console
$ docker pull kong@sha256:adad1f4a72229fe3b1768ecc601cb875a4eecb778dc0c7b2b7dc5d7f2825a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:ae3d663f065f1a138f0656708da3990b9c2c425867ef02316a929304383bc9c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49337534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf46f5ed0fbc366915b5b4809eca9e33f2ee8f2bb157565b7b5cc29d3cbcaf41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:00:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 11 Feb 2023 14:00:20 GMT
ARG ASSET=ce
# Sat, 11 Feb 2023 14:00:21 GMT
ENV ASSET=ce
# Sat, 11 Feb 2023 14:00:21 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 14:00:21 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 11 Feb 2023 14:00:21 GMT
ARG KONG_VERSION=2.8.3
# Sat, 11 Feb 2023 14:00:21 GMT
ENV KONG_VERSION=2.8.3
# Fri, 17 Feb 2023 21:05:31 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Fri, 17 Feb 2023 21:05:31 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Fri, 17 Feb 2023 21:05:38 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 17 Feb 2023 21:05:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 17 Feb 2023 21:05:38 GMT
USER kong
# Fri, 17 Feb 2023 21:05:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 17 Feb 2023 21:05:39 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 17 Feb 2023 21:05:39 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Feb 2023 21:05:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 17 Feb 2023 21:05:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332cd90dd99acdafaf1be5f2ecbf3e7e8dbb56063cd31b47aa5c172fa53f18ba`  
		Last Modified: Sat, 11 Feb 2023 14:02:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e07d8ee8b056e5949e66ecb76724024fbe556f6f36213dd16ed398f04d20db`  
		Last Modified: Fri, 17 Feb 2023 21:06:17 GMT  
		Size: 46.5 MB (46528761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baccb83225b8a3c516fb22973594a6c72238b6614bebabc09830855eab5657bf`  
		Last Modified: Fri, 17 Feb 2023 21:06:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0b6ad885b3b5ebbd99cfc0c50d4584c49e1ceb1055ccbf71a01b1dfa90c5710e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48522073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24de28b355427f0db0e877d9a43e65156a2e3b645f19b0fbc418219e4c3360e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:50 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 10 Feb 2023 22:57:50 GMT
ARG ASSET=ce
# Fri, 10 Feb 2023 22:57:50 GMT
ENV ASSET=ce
# Fri, 10 Feb 2023 22:57:50 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:51 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 10 Feb 2023 22:57:51 GMT
ARG KONG_VERSION=2.8.3
# Fri, 10 Feb 2023 22:57:51 GMT
ENV KONG_VERSION=2.8.3
# Fri, 17 Feb 2023 23:06:33 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Fri, 17 Feb 2023 23:06:33 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Fri, 17 Feb 2023 23:06:39 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 17 Feb 2023 23:06:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 17 Feb 2023 23:06:40 GMT
USER kong
# Fri, 17 Feb 2023 23:06:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 17 Feb 2023 23:06:40 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 17 Feb 2023 23:06:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Feb 2023 23:06:40 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 17 Feb 2023 23:06:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6251f58952598f508c63c9b905a49fd6e3eced7a7b48980335da9d6b1f66c342`  
		Last Modified: Fri, 17 Feb 2023 23:08:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237c69ba3586458df1a5d9283467b62823f7743cbe26455c26f395956626268e`  
		Last Modified: Fri, 17 Feb 2023 23:08:42 GMT  
		Size: 45.8 MB (45811562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46fd2edc60f47ed1ba71e37abbfdc128d1208c27da478708b44e00fe588680`  
		Last Modified: Fri, 17 Feb 2023 23:08:36 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:f1798583cd92bc873b0a2f6d37c228cbab369ee7c9a1e2b0c4c2963dfbce991d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8941ed634110902acce3a3028d346d6b3a717456dbc450e7dcb53b1e44e88763
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119175133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316afdbbfed458e79fb7703db2ea5c5ee5d2e9b9af3daf72d0a90f440044ed79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:00 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:02 GMT
ADD file:66eb2ef5574cdf80bc0cb3af1637407620c1869f58cc7514395e3f5aea45cc3b in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:39:40 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 04:39:40 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 04:39:40 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 04:39:40 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 02 Mar 2023 04:39:40 GMT
ARG KONG_VERSION=2.8.3
# Thu, 02 Mar 2023 04:39:40 GMT
ENV KONG_VERSION=2.8.3
# Thu, 02 Mar 2023 04:39:40 GMT
ARG KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810
# Thu, 02 Mar 2023 04:39:40 GMT
ARG KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
# Thu, 02 Mar 2023 04:40:08 GMT
# ARGS: KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810 KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 04:40:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 04:40:09 GMT
USER kong
# Thu, 02 Mar 2023 04:40:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 04:40:10 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 04:40:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 04:40:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 04:40:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0064b1b97ec0775813740e8cb92821a6d84fd38eee70bafba9c12d9c37534661`  
		Last Modified: Wed, 01 Mar 2023 13:18:18 GMT  
		Size: 26.7 MB (26711153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d996ec25df9553ca8d6ce43d5170ad69ba5de39cd4d25cb6f6f7b4a2ecd76e6`  
		Last Modified: Thu, 02 Mar 2023 04:41:19 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b33291cc8c0cb6cf2735a32f79d34af2914b7f6f342caa3231da5d051e1b6e`  
		Last Modified: Thu, 02 Mar 2023 04:41:28 GMT  
		Size: 67.4 MB (67381145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47aa056d40f2a0209574b485ef3bac9fd90e0009d327d2cad7e02c1f9ad135d`  
		Last Modified: Thu, 02 Mar 2023 04:41:17 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:afcd8459980b4bb0b107ece555893b162163d6efeb15c512a5849c1daa521407
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112824928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3daf60e5802a05cb80a26e3992b56fda91cc2e6093412c99a2f6cb88005926`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:05:22 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 03:05:22 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 03:05:22 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 03:05:22 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 02 Mar 2023 03:05:22 GMT
ARG KONG_VERSION=2.8.3
# Thu, 02 Mar 2023 03:05:22 GMT
ENV KONG_VERSION=2.8.3
# Thu, 02 Mar 2023 03:05:22 GMT
ARG KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810
# Thu, 02 Mar 2023 03:05:22 GMT
ARG KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
# Thu, 02 Mar 2023 03:06:14 GMT
# ARGS: KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810 KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 03:06:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 03:06:15 GMT
USER kong
# Thu, 02 Mar 2023 03:06:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:06:15 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 03:06:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 03:06:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 03:06:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9de1bca73074c336fb93a7688a40903c720a195929a0da27bd4ea424d5817c78`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 23.7 MB (23733538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac70280ff84f11c2993acdc9aadad0e9b473fe2583c43955556e661bbaba038`  
		Last Modified: Thu, 02 Mar 2023 03:07:25 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1abf765fef3776e777875fc86d62876bde0acfef424407bb55661e348b45410`  
		Last Modified: Thu, 02 Mar 2023 03:07:32 GMT  
		Size: 64.0 MB (64008556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dc6b0a55635273df167767fefcb5c1f5c2b276a4f699ae8e7a47ebfb13e5ea`  
		Last Modified: Thu, 02 Mar 2023 03:07:23 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.3`

```console
$ docker pull kong@sha256:adad1f4a72229fe3b1768ecc601cb875a4eecb778dc0c7b2b7dc5d7f2825a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.3` - linux; amd64

```console
$ docker pull kong@sha256:ae3d663f065f1a138f0656708da3990b9c2c425867ef02316a929304383bc9c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49337534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf46f5ed0fbc366915b5b4809eca9e33f2ee8f2bb157565b7b5cc29d3cbcaf41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:00:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 11 Feb 2023 14:00:20 GMT
ARG ASSET=ce
# Sat, 11 Feb 2023 14:00:21 GMT
ENV ASSET=ce
# Sat, 11 Feb 2023 14:00:21 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 14:00:21 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 11 Feb 2023 14:00:21 GMT
ARG KONG_VERSION=2.8.3
# Sat, 11 Feb 2023 14:00:21 GMT
ENV KONG_VERSION=2.8.3
# Fri, 17 Feb 2023 21:05:31 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Fri, 17 Feb 2023 21:05:31 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Fri, 17 Feb 2023 21:05:38 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 17 Feb 2023 21:05:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 17 Feb 2023 21:05:38 GMT
USER kong
# Fri, 17 Feb 2023 21:05:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 17 Feb 2023 21:05:39 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 17 Feb 2023 21:05:39 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Feb 2023 21:05:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 17 Feb 2023 21:05:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332cd90dd99acdafaf1be5f2ecbf3e7e8dbb56063cd31b47aa5c172fa53f18ba`  
		Last Modified: Sat, 11 Feb 2023 14:02:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e07d8ee8b056e5949e66ecb76724024fbe556f6f36213dd16ed398f04d20db`  
		Last Modified: Fri, 17 Feb 2023 21:06:17 GMT  
		Size: 46.5 MB (46528761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baccb83225b8a3c516fb22973594a6c72238b6614bebabc09830855eab5657bf`  
		Last Modified: Fri, 17 Feb 2023 21:06:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0b6ad885b3b5ebbd99cfc0c50d4584c49e1ceb1055ccbf71a01b1dfa90c5710e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48522073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24de28b355427f0db0e877d9a43e65156a2e3b645f19b0fbc418219e4c3360e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:50 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 10 Feb 2023 22:57:50 GMT
ARG ASSET=ce
# Fri, 10 Feb 2023 22:57:50 GMT
ENV ASSET=ce
# Fri, 10 Feb 2023 22:57:50 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:51 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 10 Feb 2023 22:57:51 GMT
ARG KONG_VERSION=2.8.3
# Fri, 10 Feb 2023 22:57:51 GMT
ENV KONG_VERSION=2.8.3
# Fri, 17 Feb 2023 23:06:33 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Fri, 17 Feb 2023 23:06:33 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Fri, 17 Feb 2023 23:06:39 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 17 Feb 2023 23:06:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 17 Feb 2023 23:06:40 GMT
USER kong
# Fri, 17 Feb 2023 23:06:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 17 Feb 2023 23:06:40 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 17 Feb 2023 23:06:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Feb 2023 23:06:40 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 17 Feb 2023 23:06:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6251f58952598f508c63c9b905a49fd6e3eced7a7b48980335da9d6b1f66c342`  
		Last Modified: Fri, 17 Feb 2023 23:08:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237c69ba3586458df1a5d9283467b62823f7743cbe26455c26f395956626268e`  
		Last Modified: Fri, 17 Feb 2023 23:08:42 GMT  
		Size: 45.8 MB (45811562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46fd2edc60f47ed1ba71e37abbfdc128d1208c27da478708b44e00fe588680`  
		Last Modified: Fri, 17 Feb 2023 23:08:36 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.3-alpine`

```console
$ docker pull kong@sha256:adad1f4a72229fe3b1768ecc601cb875a4eecb778dc0c7b2b7dc5d7f2825a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:ae3d663f065f1a138f0656708da3990b9c2c425867ef02316a929304383bc9c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49337534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf46f5ed0fbc366915b5b4809eca9e33f2ee8f2bb157565b7b5cc29d3cbcaf41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:00:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 11 Feb 2023 14:00:20 GMT
ARG ASSET=ce
# Sat, 11 Feb 2023 14:00:21 GMT
ENV ASSET=ce
# Sat, 11 Feb 2023 14:00:21 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 14:00:21 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 11 Feb 2023 14:00:21 GMT
ARG KONG_VERSION=2.8.3
# Sat, 11 Feb 2023 14:00:21 GMT
ENV KONG_VERSION=2.8.3
# Fri, 17 Feb 2023 21:05:31 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Fri, 17 Feb 2023 21:05:31 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Fri, 17 Feb 2023 21:05:38 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 17 Feb 2023 21:05:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 17 Feb 2023 21:05:38 GMT
USER kong
# Fri, 17 Feb 2023 21:05:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 17 Feb 2023 21:05:39 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 17 Feb 2023 21:05:39 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Feb 2023 21:05:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 17 Feb 2023 21:05:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332cd90dd99acdafaf1be5f2ecbf3e7e8dbb56063cd31b47aa5c172fa53f18ba`  
		Last Modified: Sat, 11 Feb 2023 14:02:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e07d8ee8b056e5949e66ecb76724024fbe556f6f36213dd16ed398f04d20db`  
		Last Modified: Fri, 17 Feb 2023 21:06:17 GMT  
		Size: 46.5 MB (46528761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baccb83225b8a3c516fb22973594a6c72238b6614bebabc09830855eab5657bf`  
		Last Modified: Fri, 17 Feb 2023 21:06:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.3-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0b6ad885b3b5ebbd99cfc0c50d4584c49e1ceb1055ccbf71a01b1dfa90c5710e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48522073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24de28b355427f0db0e877d9a43e65156a2e3b645f19b0fbc418219e4c3360e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:50 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 10 Feb 2023 22:57:50 GMT
ARG ASSET=ce
# Fri, 10 Feb 2023 22:57:50 GMT
ENV ASSET=ce
# Fri, 10 Feb 2023 22:57:50 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:51 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 10 Feb 2023 22:57:51 GMT
ARG KONG_VERSION=2.8.3
# Fri, 10 Feb 2023 22:57:51 GMT
ENV KONG_VERSION=2.8.3
# Fri, 17 Feb 2023 23:06:33 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Fri, 17 Feb 2023 23:06:33 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Fri, 17 Feb 2023 23:06:39 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 17 Feb 2023 23:06:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 17 Feb 2023 23:06:40 GMT
USER kong
# Fri, 17 Feb 2023 23:06:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 17 Feb 2023 23:06:40 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 17 Feb 2023 23:06:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Feb 2023 23:06:40 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 17 Feb 2023 23:06:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6251f58952598f508c63c9b905a49fd6e3eced7a7b48980335da9d6b1f66c342`  
		Last Modified: Fri, 17 Feb 2023 23:08:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237c69ba3586458df1a5d9283467b62823f7743cbe26455c26f395956626268e`  
		Last Modified: Fri, 17 Feb 2023 23:08:42 GMT  
		Size: 45.8 MB (45811562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e46fd2edc60f47ed1ba71e37abbfdc128d1208c27da478708b44e00fe588680`  
		Last Modified: Fri, 17 Feb 2023 23:08:36 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.3-ubuntu`

```console
$ docker pull kong@sha256:f1798583cd92bc873b0a2f6d37c228cbab369ee7c9a1e2b0c4c2963dfbce991d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8941ed634110902acce3a3028d346d6b3a717456dbc450e7dcb53b1e44e88763
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119175133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316afdbbfed458e79fb7703db2ea5c5ee5d2e9b9af3daf72d0a90f440044ed79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:00 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:02 GMT
ADD file:66eb2ef5574cdf80bc0cb3af1637407620c1869f58cc7514395e3f5aea45cc3b in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:39:40 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 04:39:40 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 04:39:40 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 04:39:40 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 02 Mar 2023 04:39:40 GMT
ARG KONG_VERSION=2.8.3
# Thu, 02 Mar 2023 04:39:40 GMT
ENV KONG_VERSION=2.8.3
# Thu, 02 Mar 2023 04:39:40 GMT
ARG KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810
# Thu, 02 Mar 2023 04:39:40 GMT
ARG KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
# Thu, 02 Mar 2023 04:40:08 GMT
# ARGS: KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810 KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 04:40:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 04:40:09 GMT
USER kong
# Thu, 02 Mar 2023 04:40:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 04:40:10 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 04:40:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 04:40:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 04:40:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0064b1b97ec0775813740e8cb92821a6d84fd38eee70bafba9c12d9c37534661`  
		Last Modified: Wed, 01 Mar 2023 13:18:18 GMT  
		Size: 26.7 MB (26711153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d996ec25df9553ca8d6ce43d5170ad69ba5de39cd4d25cb6f6f7b4a2ecd76e6`  
		Last Modified: Thu, 02 Mar 2023 04:41:19 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b33291cc8c0cb6cf2735a32f79d34af2914b7f6f342caa3231da5d051e1b6e`  
		Last Modified: Thu, 02 Mar 2023 04:41:28 GMT  
		Size: 67.4 MB (67381145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47aa056d40f2a0209574b485ef3bac9fd90e0009d327d2cad7e02c1f9ad135d`  
		Last Modified: Thu, 02 Mar 2023 04:41:17 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:afcd8459980b4bb0b107ece555893b162163d6efeb15c512a5849c1daa521407
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112824928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3daf60e5802a05cb80a26e3992b56fda91cc2e6093412c99a2f6cb88005926`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:05:22 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 03:05:22 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 03:05:22 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 03:05:22 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 02 Mar 2023 03:05:22 GMT
ARG KONG_VERSION=2.8.3
# Thu, 02 Mar 2023 03:05:22 GMT
ENV KONG_VERSION=2.8.3
# Thu, 02 Mar 2023 03:05:22 GMT
ARG KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810
# Thu, 02 Mar 2023 03:05:22 GMT
ARG KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
# Thu, 02 Mar 2023 03:06:14 GMT
# ARGS: KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810 KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 03:06:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 03:06:15 GMT
USER kong
# Thu, 02 Mar 2023 03:06:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:06:15 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 03:06:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 03:06:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 03:06:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9de1bca73074c336fb93a7688a40903c720a195929a0da27bd4ea424d5817c78`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 23.7 MB (23733538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac70280ff84f11c2993acdc9aadad0e9b473fe2583c43955556e661bbaba038`  
		Last Modified: Thu, 02 Mar 2023 03:07:25 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1abf765fef3776e777875fc86d62876bde0acfef424407bb55661e348b45410`  
		Last Modified: Thu, 02 Mar 2023 03:07:32 GMT  
		Size: 64.0 MB (64008556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dc6b0a55635273df167767fefcb5c1f5c2b276a4f699ae8e7a47ebfb13e5ea`  
		Last Modified: Thu, 02 Mar 2023 03:07:23 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3`

```console
$ docker pull kong@sha256:f97a5087ba9331c9ae2e78707df9eed51954f28d83f04358a120e2440ef05eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:36258c1d9dd6f5da8cc0403af4650f5d95296e48f83e330ec8f5fd3e3883f162
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75689080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76469f8b580bfa16be2cce693e879f0c97cf21dab83dca21aa46b9597ed0747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ENV KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 11 Feb 2023 13:59:53 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 13:59:53 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 13:59:53 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:01 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:01 GMT
USER kong
# Sat, 11 Feb 2023 14:00:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:01 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:01 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256d8d79435b0bcc04e2462111b09b5a21093f05b20ff38b484036c091891ff2`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8a6c1e7dd831b077e9ed68a8dd90af0a86718c8e0873c8c3dd6f877dc08ded`  
		Last Modified: Sat, 11 Feb 2023 14:01:56 GMT  
		Size: 72.9 MB (72880307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce630ba9f4f76fa8c33b114ce2e01fe176acd00019a99c6e2c8d9f95c2157de`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6cb2e58647fc834e751ed3ff2618757f854e8eea6baa9872b241a5b4922cd2f9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73705071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b194d85727fe1e9c5e8b3df6cfc7434c14b7c9f32b9a179c5b02f56eeced8861`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ENV KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 10 Feb 2023 22:57:24 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:25 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:25 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:31 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:32 GMT
USER kong
# Fri, 10 Feb 2023 22:57:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:32 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d673d809eb0c188ffdf72da404979eec54eac371b562252cfc579c3d1663f`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc02867f544f9cde11ef414aceb1bdd1235a8da723f6795fe0d358ecd90638`  
		Last Modified: Fri, 10 Feb 2023 23:01:13 GMT  
		Size: 71.0 MB (70994554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf15059d665b9ba5f1604f250bc942cb91274a0115c4067ea8cc0887869519`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0`

```console
$ docker pull kong@sha256:ed2dd3b2712ac3ff20dbdc82d5c20f879f379ca738dd0a922847dab51ba6f73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0` - linux; amd64

```console
$ docker pull kong@sha256:5c2c8369e9e86df300cd7eaf81c5e2c00e42982ce9121d7d8ce720d9c1fc4186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75644128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd658eaac3acd2573b99af069af18e0cb6eb943b876e551be3f48078aace6dd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_VERSION=3.0.2
# Sat, 11 Feb 2023 14:00:07 GMT
ENV KONG_VERSION=3.0.2
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Sat, 11 Feb 2023 14:00:07 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 14:00:07 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 14:00:07 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:15 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:16 GMT
USER kong
# Sat, 11 Feb 2023 14:00:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:16 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:16 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc445c500c7e2969a0df10c742d1f08b399e9183e7dbc626be205477aee2c52`  
		Last Modified: Sat, 11 Feb 2023 14:02:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79380bdff2a24981734ba5da4898b9a0c18f05842cabede3f6ec945a12eb02d1`  
		Last Modified: Sat, 11 Feb 2023 14:02:21 GMT  
		Size: 72.8 MB (72835351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695f8a90b9c4497448ae194928af5052b42aa0d708895019b4d6415d5591e1e`  
		Last Modified: Sat, 11 Feb 2023 14:02:13 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7df485332188842c5b2c958c4e261815f187b742c9b524876444a8b9d9e9d805
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73632145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7984ea834ae8b2ade0dd8bd6b1db4e9129712bb76067b9736052f34387190e23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_VERSION=3.0.2
# Fri, 10 Feb 2023 22:57:37 GMT
ENV KONG_VERSION=3.0.2
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Fri, 10 Feb 2023 22:57:37 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:37 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:37 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:45 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:45 GMT
USER kong
# Fri, 10 Feb 2023 22:57:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4f79effaded08ffc458dcd0b8666b376c40b38d1f8fc32e985a36e40c3d3e`  
		Last Modified: Fri, 10 Feb 2023 23:01:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60c99787c1181135a451bcc085437887f84003ec3641e2807e332331b11071c`  
		Last Modified: Fri, 10 Feb 2023 23:01:41 GMT  
		Size: 70.9 MB (70921631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf39f263f853308176746bf2be8939c16a2c9e1465efcdd42debcee7262357dc`  
		Last Modified: Fri, 10 Feb 2023 23:01:34 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0-alpine`

```console
$ docker pull kong@sha256:ed2dd3b2712ac3ff20dbdc82d5c20f879f379ca738dd0a922847dab51ba6f73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:5c2c8369e9e86df300cd7eaf81c5e2c00e42982ce9121d7d8ce720d9c1fc4186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75644128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd658eaac3acd2573b99af069af18e0cb6eb943b876e551be3f48078aace6dd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_VERSION=3.0.2
# Sat, 11 Feb 2023 14:00:07 GMT
ENV KONG_VERSION=3.0.2
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Sat, 11 Feb 2023 14:00:07 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 14:00:07 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 14:00:07 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:15 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:16 GMT
USER kong
# Sat, 11 Feb 2023 14:00:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:16 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:16 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc445c500c7e2969a0df10c742d1f08b399e9183e7dbc626be205477aee2c52`  
		Last Modified: Sat, 11 Feb 2023 14:02:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79380bdff2a24981734ba5da4898b9a0c18f05842cabede3f6ec945a12eb02d1`  
		Last Modified: Sat, 11 Feb 2023 14:02:21 GMT  
		Size: 72.8 MB (72835351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695f8a90b9c4497448ae194928af5052b42aa0d708895019b4d6415d5591e1e`  
		Last Modified: Sat, 11 Feb 2023 14:02:13 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7df485332188842c5b2c958c4e261815f187b742c9b524876444a8b9d9e9d805
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73632145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7984ea834ae8b2ade0dd8bd6b1db4e9129712bb76067b9736052f34387190e23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_VERSION=3.0.2
# Fri, 10 Feb 2023 22:57:37 GMT
ENV KONG_VERSION=3.0.2
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Fri, 10 Feb 2023 22:57:37 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:37 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:37 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:45 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:45 GMT
USER kong
# Fri, 10 Feb 2023 22:57:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4f79effaded08ffc458dcd0b8666b376c40b38d1f8fc32e985a36e40c3d3e`  
		Last Modified: Fri, 10 Feb 2023 23:01:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60c99787c1181135a451bcc085437887f84003ec3641e2807e332331b11071c`  
		Last Modified: Fri, 10 Feb 2023 23:01:41 GMT  
		Size: 70.9 MB (70921631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf39f263f853308176746bf2be8939c16a2c9e1465efcdd42debcee7262357dc`  
		Last Modified: Fri, 10 Feb 2023 23:01:34 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0-ubuntu`

```console
$ docker pull kong@sha256:ad48c5081f0a1fc15225400efda7826eadb1555e6ebf25deef39463dc07f5af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:820099921800ec3c85979ef2fa55fc3291c2e1ae1140ecd77133083e9de004e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101695304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a992342bbe878185b3604b552dcdd7619aae04de97f631e48fb4a45ba7e84c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:38:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 04:38:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 04:38:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 04:39:09 GMT
ARG KONG_VERSION=3.0.2
# Thu, 02 Mar 2023 04:39:09 GMT
ENV KONG_VERSION=3.0.2
# Thu, 02 Mar 2023 04:39:09 GMT
ARG KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396
# Thu, 02 Mar 2023 04:39:09 GMT
ARG KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
# Thu, 02 Mar 2023 04:39:31 GMT
# ARGS: KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396 KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 04:39:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 04:39:32 GMT
USER kong
# Thu, 02 Mar 2023 04:39:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 04:39:32 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 04:39:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 04:39:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 04:39:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0779709adcf669094932a64127d1d130f818b61ed2920768268eb7652a67df23`  
		Last Modified: Thu, 02 Mar 2023 04:40:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4ef24113b725cde8a91cc64e4fd37b056e1d5cdef86e4fee6c99675172bc5a`  
		Last Modified: Thu, 02 Mar 2023 04:41:07 GMT  
		Size: 73.1 MB (73116293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23eea2abd0f19ecdae4e8e7235fb556e76adc89e01779a7dfe6369abe7df019`  
		Last Modified: Thu, 02 Mar 2023 04:40:56 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4d64b04c043cbe187605ef5f3c412c934c110e7b2628fbda0a6a75707c47f3e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98935150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62afa556037e36d2180872c71c9d3ce6b995cb564f12a3a840c7a1eda7bcae84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:04:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 03:04:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 03:04:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 03:04:27 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 03:04:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 03:04:56 GMT
ARG KONG_VERSION=3.0.2
# Thu, 02 Mar 2023 03:04:56 GMT
ENV KONG_VERSION=3.0.2
# Thu, 02 Mar 2023 03:04:56 GMT
ARG KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396
# Thu, 02 Mar 2023 03:04:57 GMT
ARG KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
# Thu, 02 Mar 2023 03:05:13 GMT
# ARGS: KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396 KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 03:05:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 03:05:15 GMT
USER kong
# Thu, 02 Mar 2023 03:05:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:05:15 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 03:05:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 03:05:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 03:05:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d0fbc8d9bf568f12a72ae3807d56d02d576297b3b60a7cb35c92037eed9cb7`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6324ff216c7b44cafcb21a6c98e9a0aa098930e3460043fb0e5414c230b91be7`  
		Last Modified: Thu, 02 Mar 2023 03:07:14 GMT  
		Size: 71.7 MB (71739619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4fefc7101212d1aaa47e1247dc4d31fca66ff5614dc7d00b803bafde86e78b`  
		Last Modified: Thu, 02 Mar 2023 03:07:05 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.2`

```console
$ docker pull kong@sha256:ed2dd3b2712ac3ff20dbdc82d5c20f879f379ca738dd0a922847dab51ba6f73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.2` - linux; amd64

```console
$ docker pull kong@sha256:5c2c8369e9e86df300cd7eaf81c5e2c00e42982ce9121d7d8ce720d9c1fc4186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75644128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd658eaac3acd2573b99af069af18e0cb6eb943b876e551be3f48078aace6dd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_VERSION=3.0.2
# Sat, 11 Feb 2023 14:00:07 GMT
ENV KONG_VERSION=3.0.2
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Sat, 11 Feb 2023 14:00:07 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 14:00:07 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 14:00:07 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:15 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:16 GMT
USER kong
# Sat, 11 Feb 2023 14:00:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:16 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:16 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc445c500c7e2969a0df10c742d1f08b399e9183e7dbc626be205477aee2c52`  
		Last Modified: Sat, 11 Feb 2023 14:02:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79380bdff2a24981734ba5da4898b9a0c18f05842cabede3f6ec945a12eb02d1`  
		Last Modified: Sat, 11 Feb 2023 14:02:21 GMT  
		Size: 72.8 MB (72835351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695f8a90b9c4497448ae194928af5052b42aa0d708895019b4d6415d5591e1e`  
		Last Modified: Sat, 11 Feb 2023 14:02:13 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7df485332188842c5b2c958c4e261815f187b742c9b524876444a8b9d9e9d805
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73632145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7984ea834ae8b2ade0dd8bd6b1db4e9129712bb76067b9736052f34387190e23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_VERSION=3.0.2
# Fri, 10 Feb 2023 22:57:37 GMT
ENV KONG_VERSION=3.0.2
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Fri, 10 Feb 2023 22:57:37 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:37 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:37 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:45 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:45 GMT
USER kong
# Fri, 10 Feb 2023 22:57:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4f79effaded08ffc458dcd0b8666b376c40b38d1f8fc32e985a36e40c3d3e`  
		Last Modified: Fri, 10 Feb 2023 23:01:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60c99787c1181135a451bcc085437887f84003ec3641e2807e332331b11071c`  
		Last Modified: Fri, 10 Feb 2023 23:01:41 GMT  
		Size: 70.9 MB (70921631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf39f263f853308176746bf2be8939c16a2c9e1465efcdd42debcee7262357dc`  
		Last Modified: Fri, 10 Feb 2023 23:01:34 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.2-alpine`

```console
$ docker pull kong@sha256:ed2dd3b2712ac3ff20dbdc82d5c20f879f379ca738dd0a922847dab51ba6f73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:5c2c8369e9e86df300cd7eaf81c5e2c00e42982ce9121d7d8ce720d9c1fc4186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75644128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd658eaac3acd2573b99af069af18e0cb6eb943b876e551be3f48078aace6dd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_VERSION=3.0.2
# Sat, 11 Feb 2023 14:00:07 GMT
ENV KONG_VERSION=3.0.2
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Sat, 11 Feb 2023 14:00:07 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Sat, 11 Feb 2023 14:00:07 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 14:00:07 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 14:00:07 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:15 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:16 GMT
USER kong
# Sat, 11 Feb 2023 14:00:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:16 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:16 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc445c500c7e2969a0df10c742d1f08b399e9183e7dbc626be205477aee2c52`  
		Last Modified: Sat, 11 Feb 2023 14:02:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79380bdff2a24981734ba5da4898b9a0c18f05842cabede3f6ec945a12eb02d1`  
		Last Modified: Sat, 11 Feb 2023 14:02:21 GMT  
		Size: 72.8 MB (72835351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695f8a90b9c4497448ae194928af5052b42aa0d708895019b4d6415d5591e1e`  
		Last Modified: Sat, 11 Feb 2023 14:02:13 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7df485332188842c5b2c958c4e261815f187b742c9b524876444a8b9d9e9d805
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73632145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7984ea834ae8b2ade0dd8bd6b1db4e9129712bb76067b9736052f34387190e23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_VERSION=3.0.2
# Fri, 10 Feb 2023 22:57:37 GMT
ENV KONG_VERSION=3.0.2
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Fri, 10 Feb 2023 22:57:37 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Fri, 10 Feb 2023 22:57:37 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:37 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:37 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:45 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:45 GMT
USER kong
# Fri, 10 Feb 2023 22:57:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4f79effaded08ffc458dcd0b8666b376c40b38d1f8fc32e985a36e40c3d3e`  
		Last Modified: Fri, 10 Feb 2023 23:01:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60c99787c1181135a451bcc085437887f84003ec3641e2807e332331b11071c`  
		Last Modified: Fri, 10 Feb 2023 23:01:41 GMT  
		Size: 70.9 MB (70921631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf39f263f853308176746bf2be8939c16a2c9e1465efcdd42debcee7262357dc`  
		Last Modified: Fri, 10 Feb 2023 23:01:34 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.2-ubuntu`

```console
$ docker pull kong@sha256:ad48c5081f0a1fc15225400efda7826eadb1555e6ebf25deef39463dc07f5af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:820099921800ec3c85979ef2fa55fc3291c2e1ae1140ecd77133083e9de004e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101695304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a992342bbe878185b3604b552dcdd7619aae04de97f631e48fb4a45ba7e84c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:38:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 04:38:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 04:38:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 04:39:09 GMT
ARG KONG_VERSION=3.0.2
# Thu, 02 Mar 2023 04:39:09 GMT
ENV KONG_VERSION=3.0.2
# Thu, 02 Mar 2023 04:39:09 GMT
ARG KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396
# Thu, 02 Mar 2023 04:39:09 GMT
ARG KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
# Thu, 02 Mar 2023 04:39:31 GMT
# ARGS: KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396 KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 04:39:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 04:39:32 GMT
USER kong
# Thu, 02 Mar 2023 04:39:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 04:39:32 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 04:39:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 04:39:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 04:39:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0779709adcf669094932a64127d1d130f818b61ed2920768268eb7652a67df23`  
		Last Modified: Thu, 02 Mar 2023 04:40:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4ef24113b725cde8a91cc64e4fd37b056e1d5cdef86e4fee6c99675172bc5a`  
		Last Modified: Thu, 02 Mar 2023 04:41:07 GMT  
		Size: 73.1 MB (73116293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23eea2abd0f19ecdae4e8e7235fb556e76adc89e01779a7dfe6369abe7df019`  
		Last Modified: Thu, 02 Mar 2023 04:40:56 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4d64b04c043cbe187605ef5f3c412c934c110e7b2628fbda0a6a75707c47f3e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98935150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62afa556037e36d2180872c71c9d3ce6b995cb564f12a3a840c7a1eda7bcae84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:04:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 03:04:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 03:04:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 03:04:27 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 03:04:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 03:04:56 GMT
ARG KONG_VERSION=3.0.2
# Thu, 02 Mar 2023 03:04:56 GMT
ENV KONG_VERSION=3.0.2
# Thu, 02 Mar 2023 03:04:56 GMT
ARG KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396
# Thu, 02 Mar 2023 03:04:57 GMT
ARG KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
# Thu, 02 Mar 2023 03:05:13 GMT
# ARGS: KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396 KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 03:05:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 03:05:15 GMT
USER kong
# Thu, 02 Mar 2023 03:05:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:05:15 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 03:05:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 03:05:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 03:05:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d0fbc8d9bf568f12a72ae3807d56d02d576297b3b60a7cb35c92037eed9cb7`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6324ff216c7b44cafcb21a6c98e9a0aa098930e3460043fb0e5414c230b91be7`  
		Last Modified: Thu, 02 Mar 2023 03:07:14 GMT  
		Size: 71.7 MB (71739619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4fefc7101212d1aaa47e1247dc4d31fca66ff5614dc7d00b803bafde86e78b`  
		Last Modified: Thu, 02 Mar 2023 03:07:05 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1`

```console
$ docker pull kong@sha256:f97a5087ba9331c9ae2e78707df9eed51954f28d83f04358a120e2440ef05eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1` - linux; amd64

```console
$ docker pull kong@sha256:36258c1d9dd6f5da8cc0403af4650f5d95296e48f83e330ec8f5fd3e3883f162
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75689080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76469f8b580bfa16be2cce693e879f0c97cf21dab83dca21aa46b9597ed0747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ENV KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 11 Feb 2023 13:59:53 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 13:59:53 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 13:59:53 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:01 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:01 GMT
USER kong
# Sat, 11 Feb 2023 14:00:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:01 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:01 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256d8d79435b0bcc04e2462111b09b5a21093f05b20ff38b484036c091891ff2`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8a6c1e7dd831b077e9ed68a8dd90af0a86718c8e0873c8c3dd6f877dc08ded`  
		Last Modified: Sat, 11 Feb 2023 14:01:56 GMT  
		Size: 72.9 MB (72880307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce630ba9f4f76fa8c33b114ce2e01fe176acd00019a99c6e2c8d9f95c2157de`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6cb2e58647fc834e751ed3ff2618757f854e8eea6baa9872b241a5b4922cd2f9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73705071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b194d85727fe1e9c5e8b3df6cfc7434c14b7c9f32b9a179c5b02f56eeced8861`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ENV KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 10 Feb 2023 22:57:24 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:25 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:25 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:31 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:32 GMT
USER kong
# Fri, 10 Feb 2023 22:57:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:32 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d673d809eb0c188ffdf72da404979eec54eac371b562252cfc579c3d1663f`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc02867f544f9cde11ef414aceb1bdd1235a8da723f6795fe0d358ecd90638`  
		Last Modified: Fri, 10 Feb 2023 23:01:13 GMT  
		Size: 71.0 MB (70994554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf15059d665b9ba5f1604f250bc942cb91274a0115c4067ea8cc0887869519`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1-ubuntu`

```console
$ docker pull kong@sha256:59ac8f8aafe1cd3ec4b39327c5c19419ec28f314c6da013e24d33c012ea6085e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e15d813b435a4b18871610a9d3dfa61d934433ec1322c590beec599b13fb3adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101732390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40416b0838ed86aa1c69b3dd31c81af858550972c1cc6ff8a5049f8967b3837a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:38:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 04:38:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 04:38:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 04:38:27 GMT
ARG KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 04:38:27 GMT
ENV KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 04:38:27 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Thu, 02 Mar 2023 04:38:27 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Thu, 02 Mar 2023 04:39:01 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 04:39:02 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 04:39:02 GMT
USER kong
# Thu, 02 Mar 2023 04:39:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 04:39:02 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 04:39:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 04:39:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 04:39:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0779709adcf669094932a64127d1d130f818b61ed2920768268eb7652a67df23`  
		Last Modified: Thu, 02 Mar 2023 04:40:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387f2b1287f2c648cab435546c885fa589f3fa5db0477665e67f511130949603`  
		Last Modified: Thu, 02 Mar 2023 04:40:45 GMT  
		Size: 73.2 MB (73153381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf3d6a2821274103cdd89cc8bae4e9f40224d3f8d0208b8bfa403ce950a30bf`  
		Last Modified: Thu, 02 Mar 2023 04:40:33 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f37cdf0d55daae01c871ce3190bb98ee4ad1cf665a5d5908567ccc518a2343eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98967418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71af4a27e17d09b757d37e788f1396d8e93c875e4bba189e4e6247583f63e90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:04:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 03:04:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 03:04:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 03:04:27 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 03:04:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 03:04:27 GMT
ENV KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Thu, 02 Mar 2023 03:04:48 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 03:04:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 03:04:49 GMT
USER kong
# Thu, 02 Mar 2023 03:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:04:49 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 03:04:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 03:04:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 03:04:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d0fbc8d9bf568f12a72ae3807d56d02d576297b3b60a7cb35c92037eed9cb7`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f420840a76159d996c9e294e0e41d81735ac1c72051f3338e7fc4441119b8b`  
		Last Modified: Thu, 02 Mar 2023 03:06:53 GMT  
		Size: 71.8 MB (71771888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eff32e2df689b166673a2995418859a7ba334495d8b03f94c502f2b6183fc1a`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1`

```console
$ docker pull kong@sha256:f97a5087ba9331c9ae2e78707df9eed51954f28d83f04358a120e2440ef05eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1` - linux; amd64

```console
$ docker pull kong@sha256:36258c1d9dd6f5da8cc0403af4650f5d95296e48f83e330ec8f5fd3e3883f162
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75689080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76469f8b580bfa16be2cce693e879f0c97cf21dab83dca21aa46b9597ed0747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ENV KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 11 Feb 2023 13:59:53 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 13:59:53 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 13:59:53 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:01 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:01 GMT
USER kong
# Sat, 11 Feb 2023 14:00:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:01 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:01 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256d8d79435b0bcc04e2462111b09b5a21093f05b20ff38b484036c091891ff2`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8a6c1e7dd831b077e9ed68a8dd90af0a86718c8e0873c8c3dd6f877dc08ded`  
		Last Modified: Sat, 11 Feb 2023 14:01:56 GMT  
		Size: 72.9 MB (72880307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce630ba9f4f76fa8c33b114ce2e01fe176acd00019a99c6e2c8d9f95c2157de`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6cb2e58647fc834e751ed3ff2618757f854e8eea6baa9872b241a5b4922cd2f9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73705071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b194d85727fe1e9c5e8b3df6cfc7434c14b7c9f32b9a179c5b02f56eeced8861`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ENV KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 10 Feb 2023 22:57:24 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:25 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:25 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:31 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:32 GMT
USER kong
# Fri, 10 Feb 2023 22:57:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:32 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d673d809eb0c188ffdf72da404979eec54eac371b562252cfc579c3d1663f`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc02867f544f9cde11ef414aceb1bdd1235a8da723f6795fe0d358ecd90638`  
		Last Modified: Fri, 10 Feb 2023 23:01:13 GMT  
		Size: 71.0 MB (70994554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf15059d665b9ba5f1604f250bc942cb91274a0115c4067ea8cc0887869519`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1-alpine`

```console
$ docker pull kong@sha256:f97a5087ba9331c9ae2e78707df9eed51954f28d83f04358a120e2440ef05eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:36258c1d9dd6f5da8cc0403af4650f5d95296e48f83e330ec8f5fd3e3883f162
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75689080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76469f8b580bfa16be2cce693e879f0c97cf21dab83dca21aa46b9597ed0747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ENV KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 11 Feb 2023 13:59:53 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 13:59:53 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 13:59:53 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:01 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:01 GMT
USER kong
# Sat, 11 Feb 2023 14:00:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:01 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:01 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256d8d79435b0bcc04e2462111b09b5a21093f05b20ff38b484036c091891ff2`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8a6c1e7dd831b077e9ed68a8dd90af0a86718c8e0873c8c3dd6f877dc08ded`  
		Last Modified: Sat, 11 Feb 2023 14:01:56 GMT  
		Size: 72.9 MB (72880307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce630ba9f4f76fa8c33b114ce2e01fe176acd00019a99c6e2c8d9f95c2157de`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6cb2e58647fc834e751ed3ff2618757f854e8eea6baa9872b241a5b4922cd2f9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73705071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b194d85727fe1e9c5e8b3df6cfc7434c14b7c9f32b9a179c5b02f56eeced8861`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ENV KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 10 Feb 2023 22:57:24 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:25 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:25 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:31 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:32 GMT
USER kong
# Fri, 10 Feb 2023 22:57:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:32 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d673d809eb0c188ffdf72da404979eec54eac371b562252cfc579c3d1663f`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc02867f544f9cde11ef414aceb1bdd1235a8da723f6795fe0d358ecd90638`  
		Last Modified: Fri, 10 Feb 2023 23:01:13 GMT  
		Size: 71.0 MB (70994554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf15059d665b9ba5f1604f250bc942cb91274a0115c4067ea8cc0887869519`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1-ubuntu`

```console
$ docker pull kong@sha256:59ac8f8aafe1cd3ec4b39327c5c19419ec28f314c6da013e24d33c012ea6085e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e15d813b435a4b18871610a9d3dfa61d934433ec1322c590beec599b13fb3adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101732390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40416b0838ed86aa1c69b3dd31c81af858550972c1cc6ff8a5049f8967b3837a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:38:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 04:38:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 04:38:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 04:38:27 GMT
ARG KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 04:38:27 GMT
ENV KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 04:38:27 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Thu, 02 Mar 2023 04:38:27 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Thu, 02 Mar 2023 04:39:01 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 04:39:02 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 04:39:02 GMT
USER kong
# Thu, 02 Mar 2023 04:39:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 04:39:02 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 04:39:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 04:39:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 04:39:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0779709adcf669094932a64127d1d130f818b61ed2920768268eb7652a67df23`  
		Last Modified: Thu, 02 Mar 2023 04:40:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387f2b1287f2c648cab435546c885fa589f3fa5db0477665e67f511130949603`  
		Last Modified: Thu, 02 Mar 2023 04:40:45 GMT  
		Size: 73.2 MB (73153381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf3d6a2821274103cdd89cc8bae4e9f40224d3f8d0208b8bfa403ce950a30bf`  
		Last Modified: Thu, 02 Mar 2023 04:40:33 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f37cdf0d55daae01c871ce3190bb98ee4ad1cf665a5d5908567ccc518a2343eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98967418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71af4a27e17d09b757d37e788f1396d8e93c875e4bba189e4e6247583f63e90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:04:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 03:04:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 03:04:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 03:04:27 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 03:04:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 03:04:27 GMT
ENV KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Thu, 02 Mar 2023 03:04:48 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 03:04:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 03:04:49 GMT
USER kong
# Thu, 02 Mar 2023 03:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:04:49 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 03:04:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 03:04:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 03:04:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d0fbc8d9bf568f12a72ae3807d56d02d576297b3b60a7cb35c92037eed9cb7`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f420840a76159d996c9e294e0e41d81735ac1c72051f3338e7fc4441119b8b`  
		Last Modified: Thu, 02 Mar 2023 03:06:53 GMT  
		Size: 71.8 MB (71771888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eff32e2df689b166673a2995418859a7ba334495d8b03f94c502f2b6183fc1a`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:f97a5087ba9331c9ae2e78707df9eed51954f28d83f04358a120e2440ef05eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:36258c1d9dd6f5da8cc0403af4650f5d95296e48f83e330ec8f5fd3e3883f162
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75689080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76469f8b580bfa16be2cce693e879f0c97cf21dab83dca21aa46b9597ed0747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ENV KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 11 Feb 2023 13:59:53 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 13:59:53 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 13:59:53 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:01 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:01 GMT
USER kong
# Sat, 11 Feb 2023 14:00:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:01 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:01 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256d8d79435b0bcc04e2462111b09b5a21093f05b20ff38b484036c091891ff2`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8a6c1e7dd831b077e9ed68a8dd90af0a86718c8e0873c8c3dd6f877dc08ded`  
		Last Modified: Sat, 11 Feb 2023 14:01:56 GMT  
		Size: 72.9 MB (72880307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce630ba9f4f76fa8c33b114ce2e01fe176acd00019a99c6e2c8d9f95c2157de`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6cb2e58647fc834e751ed3ff2618757f854e8eea6baa9872b241a5b4922cd2f9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73705071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b194d85727fe1e9c5e8b3df6cfc7434c14b7c9f32b9a179c5b02f56eeced8861`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ENV KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 10 Feb 2023 22:57:24 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:25 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:25 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:31 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:32 GMT
USER kong
# Fri, 10 Feb 2023 22:57:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:32 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d673d809eb0c188ffdf72da404979eec54eac371b562252cfc579c3d1663f`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc02867f544f9cde11ef414aceb1bdd1235a8da723f6795fe0d358ecd90638`  
		Last Modified: Fri, 10 Feb 2023 23:01:13 GMT  
		Size: 71.0 MB (70994554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf15059d665b9ba5f1604f250bc942cb91274a0115c4067ea8cc0887869519`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:f97a5087ba9331c9ae2e78707df9eed51954f28d83f04358a120e2440ef05eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:36258c1d9dd6f5da8cc0403af4650f5d95296e48f83e330ec8f5fd3e3883f162
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75689080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76469f8b580bfa16be2cce693e879f0c97cf21dab83dca21aa46b9597ed0747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:59:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ENV KONG_VERSION=3.1.1
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 11 Feb 2023 13:59:53 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 11 Feb 2023 13:59:53 GMT
ARG ASSET=remote
# Sat, 11 Feb 2023 13:59:53 GMT
ARG EE_PORTS
# Sat, 11 Feb 2023 13:59:53 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 11 Feb 2023 14:00:01 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 11 Feb 2023 14:00:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 11 Feb 2023 14:00:01 GMT
USER kong
# Sat, 11 Feb 2023 14:00:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 14:00:01 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 11 Feb 2023 14:00:01 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 14:00:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 11 Feb 2023 14:00:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256d8d79435b0bcc04e2462111b09b5a21093f05b20ff38b484036c091891ff2`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8a6c1e7dd831b077e9ed68a8dd90af0a86718c8e0873c8c3dd6f877dc08ded`  
		Last Modified: Sat, 11 Feb 2023 14:01:56 GMT  
		Size: 72.9 MB (72880307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce630ba9f4f76fa8c33b114ce2e01fe176acd00019a99c6e2c8d9f95c2157de`  
		Last Modified: Sat, 11 Feb 2023 14:01:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6cb2e58647fc834e751ed3ff2618757f854e8eea6baa9872b241a5b4922cd2f9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73705071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b194d85727fe1e9c5e8b3df6cfc7434c14b7c9f32b9a179c5b02f56eeced8861`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:57:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ENV KONG_VERSION=3.1.1
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 10 Feb 2023 22:57:24 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 10 Feb 2023 22:57:24 GMT
ARG ASSET=remote
# Fri, 10 Feb 2023 22:57:25 GMT
ARG EE_PORTS
# Fri, 10 Feb 2023 22:57:25 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 10 Feb 2023 22:57:31 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 10 Feb 2023 22:57:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:57:32 GMT
USER kong
# Fri, 10 Feb 2023 22:57:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:57:32 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 10 Feb 2023 22:57:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Feb 2023 22:57:32 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 10 Feb 2023 22:57:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d673d809eb0c188ffdf72da404979eec54eac371b562252cfc579c3d1663f`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc02867f544f9cde11ef414aceb1bdd1235a8da723f6795fe0d358ecd90638`  
		Last Modified: Fri, 10 Feb 2023 23:01:13 GMT  
		Size: 71.0 MB (70994554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecf15059d665b9ba5f1604f250bc942cb91274a0115c4067ea8cc0887869519`  
		Last Modified: Fri, 10 Feb 2023 23:01:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:59ac8f8aafe1cd3ec4b39327c5c19419ec28f314c6da013e24d33c012ea6085e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e15d813b435a4b18871610a9d3dfa61d934433ec1322c590beec599b13fb3adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101732390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40416b0838ed86aa1c69b3dd31c81af858550972c1cc6ff8a5049f8967b3837a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:38:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 04:38:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 04:38:26 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 04:38:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 04:38:27 GMT
ARG KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 04:38:27 GMT
ENV KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 04:38:27 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Thu, 02 Mar 2023 04:38:27 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Thu, 02 Mar 2023 04:39:01 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 04:39:02 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 04:39:02 GMT
USER kong
# Thu, 02 Mar 2023 04:39:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 04:39:02 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 04:39:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 04:39:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 04:39:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0779709adcf669094932a64127d1d130f818b61ed2920768268eb7652a67df23`  
		Last Modified: Thu, 02 Mar 2023 04:40:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387f2b1287f2c648cab435546c885fa589f3fa5db0477665e67f511130949603`  
		Last Modified: Thu, 02 Mar 2023 04:40:45 GMT  
		Size: 73.2 MB (73153381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf3d6a2821274103cdd89cc8bae4e9f40224d3f8d0208b8bfa403ce950a30bf`  
		Last Modified: Thu, 02 Mar 2023 04:40:33 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f37cdf0d55daae01c871ce3190bb98ee4ad1cf665a5d5908567ccc518a2343eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98967418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71af4a27e17d09b757d37e788f1396d8e93c875e4bba189e4e6247583f63e90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:04:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 03:04:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 03:04:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 03:04:27 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 03:04:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 03:04:27 GMT
ENV KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Thu, 02 Mar 2023 03:04:48 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 03:04:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 03:04:49 GMT
USER kong
# Thu, 02 Mar 2023 03:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:04:49 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 03:04:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 03:04:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 03:04:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d0fbc8d9bf568f12a72ae3807d56d02d576297b3b60a7cb35c92037eed9cb7`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f420840a76159d996c9e294e0e41d81735ac1c72051f3338e7fc4441119b8b`  
		Last Modified: Thu, 02 Mar 2023 03:06:53 GMT  
		Size: 71.8 MB (71771888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eff32e2df689b166673a2995418859a7ba334495d8b03f94c502f2b6183fc1a`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
