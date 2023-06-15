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
-	[`kong:3.2`](#kong32)
-	[`kong:3.2-ubuntu`](#kong32-ubuntu)
-	[`kong:3.2.2`](#kong322)
-	[`kong:3.2.2-alpine`](#kong322-alpine)
-	[`kong:3.2.2-ubuntu`](#kong322-ubuntu)
-	[`kong:3.3`](#kong33)
-	[`kong:3.3-ubuntu`](#kong33-ubuntu)
-	[`kong:3.3.0`](#kong330)
-	[`kong:3.3.0-alpine`](#kong330-alpine)
-	[`kong:3.3.0-ubuntu`](#kong330-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.8`

```console
$ docker pull kong@sha256:333d0f4d22ca495e9e376a590bb24d134e6b59175e5e77d2e11322d263b3ce21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:713789b93a0fa4081776691c27e4a9712b4c163f3c6fc3d0d8f20e988267f5e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49373331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6aa1f074244b99d59199674239b3125eed26146726d39803b7c432541c618e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 15 Jun 2023 06:25:19 GMT
ARG ASSET=ce
# Thu, 15 Jun 2023 06:25:20 GMT
ENV ASSET=ce
# Thu, 15 Jun 2023 06:25:20 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:25:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 15 Jun 2023 06:25:20 GMT
ARG KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 06:25:20 GMT
ENV KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 06:25:20 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Thu, 15 Jun 2023 06:25:20 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Thu, 15 Jun 2023 06:25:27 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 15 Jun 2023 06:25:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:25:27 GMT
USER kong
# Thu, 15 Jun 2023 06:25:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:25:27 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a3cffc76b093ccc58db04ef3355333d93f40ac3c60304ac3c451740f20380e`  
		Last Modified: Thu, 15 Jun 2023 06:27:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b68e3c47dd4a95fb01daf0c3f21056dbb306c43005ed97c9c8d537edf2ce84`  
		Last Modified: Thu, 15 Jun 2023 06:27:07 GMT  
		Size: 46.6 MB (46564649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf89364b9c0039a1ccd22f01467d98fec4250f7e4a1fd94385971ab4e1de6e67`  
		Last Modified: Thu, 15 Jun 2023 06:27:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0453ddb662f69b61f3e7dc9599818aa7086c5e1a79406e48ad2dc24de1973446
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48558546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83fb576cec3804f46d1ac467a47660530f4995293951b475a4bc5422df0e96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:42:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 15 Jun 2023 00:42:20 GMT
ARG ASSET=ce
# Thu, 15 Jun 2023 00:42:20 GMT
ENV ASSET=ce
# Thu, 15 Jun 2023 00:42:20 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:42:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 15 Jun 2023 00:42:20 GMT
ARG KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 00:42:21 GMT
ENV KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 00:42:21 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Thu, 15 Jun 2023 00:42:21 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Thu, 15 Jun 2023 00:42:27 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 15 Jun 2023 00:42:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:28 GMT
USER kong
# Thu, 15 Jun 2023 00:42:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:28 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab1b35d2d75cdc60cacfe207a2fc28581512d1e48b38519945b8d95d45cb2b`  
		Last Modified: Thu, 15 Jun 2023 00:43:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8719519dc06ae4474af38360433cae6d3875191a3fa3f99f09ac32b31c9a7b`  
		Last Modified: Thu, 15 Jun 2023 00:43:36 GMT  
		Size: 45.8 MB (45849631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2e7eaca4a2e90378e3725946eaabe938e5babee334d3482a78a36ad6eb276d`  
		Last Modified: Thu, 15 Jun 2023 00:43:29 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:bca947da1904c3f562c39dc0cd39c38b42ffe80ebf9e7e32394ef1c0c0c055cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:acf28d896192bb0a0d763bd71344dc50b464d791351fceb99870b43c48c41ad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119387329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde46139b2824b356768d354ecbef753dde3f5921acc03a1191d1cbe6123db8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:32:26 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:32:26 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:32:26 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:32:27 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:32:27 GMT
ARG KONG_VERSION=2.8.3
# Fri, 02 Jun 2023 01:32:27 GMT
ENV KONG_VERSION=2.8.3
# Fri, 02 Jun 2023 01:32:27 GMT
ARG KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810
# Fri, 02 Jun 2023 01:32:27 GMT
ARG KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
# Fri, 02 Jun 2023 01:32:53 GMT
# ARGS: KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810 KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:32:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:32:54 GMT
USER kong
# Fri, 02 Jun 2023 01:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:32:54 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:32:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:32:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:32:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6118fa5af40da97195ae6cab7e2e8f9cc05b50459ee1e1448a4e6474bf74bc29`  
		Last Modified: Fri, 02 Jun 2023 01:34:04 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe58ac5f781db246f24e1a10d7d157bcce0277b0108cf5f1bdd73d566b4b229d`  
		Last Modified: Fri, 02 Jun 2023 01:34:13 GMT  
		Size: 67.6 MB (67587122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bf88b49502f0db3e88ad85f37e8933423e31d293b64c98163e2c711ef40ab8`  
		Last Modified: Fri, 02 Jun 2023 01:34:02 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5cefac7b46d6ad7744555399726f2787e9283ea4b582080d3e61ea2a369c6d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113033786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954b1f32c76863ec51999ae69faa00474e4e8f7b2fce5e298720423e5ac9aed4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:53 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:53 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:54 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:54 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:54 GMT
ARG KONG_VERSION=2.8.3
# Thu, 01 Jun 2023 23:38:54 GMT
ENV KONG_VERSION=2.8.3
# Thu, 01 Jun 2023 23:38:54 GMT
ARG KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810
# Thu, 01 Jun 2023 23:38:54 GMT
ARG KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
# Thu, 01 Jun 2023 23:39:26 GMT
# ARGS: KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810 KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:39:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:39:27 GMT
USER kong
# Thu, 01 Jun 2023 23:39:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:39:27 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:39:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:39:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:39:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ef3d318ed811633bd8f4e109c8c3dbf7f911d5f83b67b3222b01ec4e4b0c9`  
		Last Modified: Thu, 01 Jun 2023 23:40:33 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2d1b7e8ca60037ae9795efc4985a841e2024c768ad28489971a8b39b5b8de9`  
		Last Modified: Thu, 01 Jun 2023 23:40:40 GMT  
		Size: 64.2 MB (64210045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155334a315c5daddf675e0a0421864216ef9d5b62fcfa758780ce23bc563f651`  
		Last Modified: Thu, 01 Jun 2023 23:40:31 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.3`

```console
$ docker pull kong@sha256:333d0f4d22ca495e9e376a590bb24d134e6b59175e5e77d2e11322d263b3ce21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.3` - linux; amd64

```console
$ docker pull kong@sha256:713789b93a0fa4081776691c27e4a9712b4c163f3c6fc3d0d8f20e988267f5e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49373331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6aa1f074244b99d59199674239b3125eed26146726d39803b7c432541c618e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 15 Jun 2023 06:25:19 GMT
ARG ASSET=ce
# Thu, 15 Jun 2023 06:25:20 GMT
ENV ASSET=ce
# Thu, 15 Jun 2023 06:25:20 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:25:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 15 Jun 2023 06:25:20 GMT
ARG KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 06:25:20 GMT
ENV KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 06:25:20 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Thu, 15 Jun 2023 06:25:20 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Thu, 15 Jun 2023 06:25:27 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 15 Jun 2023 06:25:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:25:27 GMT
USER kong
# Thu, 15 Jun 2023 06:25:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:25:27 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a3cffc76b093ccc58db04ef3355333d93f40ac3c60304ac3c451740f20380e`  
		Last Modified: Thu, 15 Jun 2023 06:27:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b68e3c47dd4a95fb01daf0c3f21056dbb306c43005ed97c9c8d537edf2ce84`  
		Last Modified: Thu, 15 Jun 2023 06:27:07 GMT  
		Size: 46.6 MB (46564649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf89364b9c0039a1ccd22f01467d98fec4250f7e4a1fd94385971ab4e1de6e67`  
		Last Modified: Thu, 15 Jun 2023 06:27:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0453ddb662f69b61f3e7dc9599818aa7086c5e1a79406e48ad2dc24de1973446
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48558546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83fb576cec3804f46d1ac467a47660530f4995293951b475a4bc5422df0e96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:42:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 15 Jun 2023 00:42:20 GMT
ARG ASSET=ce
# Thu, 15 Jun 2023 00:42:20 GMT
ENV ASSET=ce
# Thu, 15 Jun 2023 00:42:20 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:42:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 15 Jun 2023 00:42:20 GMT
ARG KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 00:42:21 GMT
ENV KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 00:42:21 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Thu, 15 Jun 2023 00:42:21 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Thu, 15 Jun 2023 00:42:27 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 15 Jun 2023 00:42:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:28 GMT
USER kong
# Thu, 15 Jun 2023 00:42:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:28 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab1b35d2d75cdc60cacfe207a2fc28581512d1e48b38519945b8d95d45cb2b`  
		Last Modified: Thu, 15 Jun 2023 00:43:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8719519dc06ae4474af38360433cae6d3875191a3fa3f99f09ac32b31c9a7b`  
		Last Modified: Thu, 15 Jun 2023 00:43:36 GMT  
		Size: 45.8 MB (45849631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2e7eaca4a2e90378e3725946eaabe938e5babee334d3482a78a36ad6eb276d`  
		Last Modified: Thu, 15 Jun 2023 00:43:29 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.3-alpine`

```console
$ docker pull kong@sha256:333d0f4d22ca495e9e376a590bb24d134e6b59175e5e77d2e11322d263b3ce21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:713789b93a0fa4081776691c27e4a9712b4c163f3c6fc3d0d8f20e988267f5e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49373331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6aa1f074244b99d59199674239b3125eed26146726d39803b7c432541c618e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:25:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 15 Jun 2023 06:25:19 GMT
ARG ASSET=ce
# Thu, 15 Jun 2023 06:25:20 GMT
ENV ASSET=ce
# Thu, 15 Jun 2023 06:25:20 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:25:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 15 Jun 2023 06:25:20 GMT
ARG KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 06:25:20 GMT
ENV KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 06:25:20 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Thu, 15 Jun 2023 06:25:20 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Thu, 15 Jun 2023 06:25:27 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 15 Jun 2023 06:25:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:25:27 GMT
USER kong
# Thu, 15 Jun 2023 06:25:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:25:27 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a3cffc76b093ccc58db04ef3355333d93f40ac3c60304ac3c451740f20380e`  
		Last Modified: Thu, 15 Jun 2023 06:27:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b68e3c47dd4a95fb01daf0c3f21056dbb306c43005ed97c9c8d537edf2ce84`  
		Last Modified: Thu, 15 Jun 2023 06:27:07 GMT  
		Size: 46.6 MB (46564649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf89364b9c0039a1ccd22f01467d98fec4250f7e4a1fd94385971ab4e1de6e67`  
		Last Modified: Thu, 15 Jun 2023 06:27:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.3-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0453ddb662f69b61f3e7dc9599818aa7086c5e1a79406e48ad2dc24de1973446
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48558546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83fb576cec3804f46d1ac467a47660530f4995293951b475a4bc5422df0e96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:42:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 15 Jun 2023 00:42:20 GMT
ARG ASSET=ce
# Thu, 15 Jun 2023 00:42:20 GMT
ENV ASSET=ce
# Thu, 15 Jun 2023 00:42:20 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:42:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 15 Jun 2023 00:42:20 GMT
ARG KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 00:42:21 GMT
ENV KONG_VERSION=2.8.3
# Thu, 15 Jun 2023 00:42:21 GMT
ARG KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa
# Thu, 15 Jun 2023 00:42:21 GMT
ARG KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
# Thu, 15 Jun 2023 00:42:27 GMT
# ARGS: KONG_AMD64_SHA=46e8ccd60fdcfb44a02b7ff9cfc79b701bf1275ec6ba88138d98317509c682fa KONG_ARM64_SHA=f6c90eb9b126e049859f037e81f070f4116ac701c4e4b9ad2d1ec574fbe44bb3
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 15 Jun 2023 00:42:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:28 GMT
USER kong
# Thu, 15 Jun 2023 00:42:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:28 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab1b35d2d75cdc60cacfe207a2fc28581512d1e48b38519945b8d95d45cb2b`  
		Last Modified: Thu, 15 Jun 2023 00:43:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8719519dc06ae4474af38360433cae6d3875191a3fa3f99f09ac32b31c9a7b`  
		Last Modified: Thu, 15 Jun 2023 00:43:36 GMT  
		Size: 45.8 MB (45849631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2e7eaca4a2e90378e3725946eaabe938e5babee334d3482a78a36ad6eb276d`  
		Last Modified: Thu, 15 Jun 2023 00:43:29 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.3-ubuntu`

```console
$ docker pull kong@sha256:bca947da1904c3f562c39dc0cd39c38b42ffe80ebf9e7e32394ef1c0c0c055cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:acf28d896192bb0a0d763bd71344dc50b464d791351fceb99870b43c48c41ad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119387329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde46139b2824b356768d354ecbef753dde3f5921acc03a1191d1cbe6123db8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:32:26 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:32:26 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:32:26 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:32:27 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:32:27 GMT
ARG KONG_VERSION=2.8.3
# Fri, 02 Jun 2023 01:32:27 GMT
ENV KONG_VERSION=2.8.3
# Fri, 02 Jun 2023 01:32:27 GMT
ARG KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810
# Fri, 02 Jun 2023 01:32:27 GMT
ARG KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
# Fri, 02 Jun 2023 01:32:53 GMT
# ARGS: KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810 KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:32:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:32:54 GMT
USER kong
# Fri, 02 Jun 2023 01:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:32:54 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:32:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:32:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:32:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6118fa5af40da97195ae6cab7e2e8f9cc05b50459ee1e1448a4e6474bf74bc29`  
		Last Modified: Fri, 02 Jun 2023 01:34:04 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe58ac5f781db246f24e1a10d7d157bcce0277b0108cf5f1bdd73d566b4b229d`  
		Last Modified: Fri, 02 Jun 2023 01:34:13 GMT  
		Size: 67.6 MB (67587122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bf88b49502f0db3e88ad85f37e8933423e31d293b64c98163e2c711ef40ab8`  
		Last Modified: Fri, 02 Jun 2023 01:34:02 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5cefac7b46d6ad7744555399726f2787e9283ea4b582080d3e61ea2a369c6d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113033786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954b1f32c76863ec51999ae69faa00474e4e8f7b2fce5e298720423e5ac9aed4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:53 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:53 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:54 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:54 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:54 GMT
ARG KONG_VERSION=2.8.3
# Thu, 01 Jun 2023 23:38:54 GMT
ENV KONG_VERSION=2.8.3
# Thu, 01 Jun 2023 23:38:54 GMT
ARG KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810
# Thu, 01 Jun 2023 23:38:54 GMT
ARG KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
# Thu, 01 Jun 2023 23:39:26 GMT
# ARGS: KONG_AMD64_SHA=b52baf1caa300c3ee70ff4d58982085b1da9203c69118c885f00d13954634810 KONG_ARM64_SHA=1d5c2064d44b76fbb3cabf168dc226e91fedb991ace32915297505d089679fed
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:39:27 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:39:27 GMT
USER kong
# Thu, 01 Jun 2023 23:39:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:39:27 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:39:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:39:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:39:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ef3d318ed811633bd8f4e109c8c3dbf7f911d5f83b67b3222b01ec4e4b0c9`  
		Last Modified: Thu, 01 Jun 2023 23:40:33 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2d1b7e8ca60037ae9795efc4985a841e2024c768ad28489971a8b39b5b8de9`  
		Last Modified: Thu, 01 Jun 2023 23:40:40 GMT  
		Size: 64.2 MB (64210045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155334a315c5daddf675e0a0421864216ef9d5b62fcfa758780ce23bc563f651`  
		Last Modified: Thu, 01 Jun 2023 23:40:31 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3`

```console
$ docker pull kong@sha256:9078cc4badc63e1b591ee5e8f1cd97d8a0659b7c783f5fdeeba77e0c6c78e5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:cb97b3b9bd4540d09f246f855be72a044b342bbf980c96a0b8117b2700c98ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81311313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5971887ac84cdc4ba0a9c21b9212a6b94d1970e3664b1282ebc11b1954facf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:08 GMT
ARG KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ENV KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Fri, 02 Jun 2023 01:31:42 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:31:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:31:43 GMT
USER kong
# Fri, 02 Jun 2023 01:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:31:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:31:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:31:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:31:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8937d2707ca171dddcc194356d4edef593341b55286e3b54343d1bb304f2c023`  
		Last Modified: Fri, 02 Jun 2023 01:33:24 GMT  
		Size: 50.9 MB (50879757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c105bdc14980907cff3f5de1391848b1ca553a71da5d26d71345454e918caa`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:53f32385a7bb5533c03d3dba190cb1e257b0dfd46a41f6576b0b1fd91245d0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75728888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdec04b213ff81ba8f4c88338767b36a7a4c9f8f3c61d9dbe590be96fb51491`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ENV KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Thu, 01 Jun 2023 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:25 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:25 GMT
USER kong
# Thu, 01 Jun 2023 23:38:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a99a85577e3756d8a7bd71326e7a8674934ddb169bd5a4349103e197a58f983`  
		Last Modified: Thu, 01 Jun 2023 23:39:52 GMT  
		Size: 47.3 MB (47338562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e0e212694b9b9de8b4bcbb4713dbb848f27b1198ac68df26605d26d233870c`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0`

```console
$ docker pull kong@sha256:c16f02938ab7ae019576dfc17a72e0408393b74ef5a363eb1d9f4d673bffa8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0` - linux; amd64

```console
$ docker pull kong@sha256:dbdab62f9949e0843b7d8a46740b805940c6214a78bdab5bf61d169075affbc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75644403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cde42fd180357ec474d41db513f1f83b601663b89a41dedd1b04abb9543e8fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:24:51 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 06:25:05 GMT
ARG KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 06:25:05 GMT
ENV KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 06:25:05 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Thu, 15 Jun 2023 06:25:06 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Thu, 15 Jun 2023 06:25:06 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 06:25:06 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:25:06 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 06:25:14 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 06:25:14 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:25:14 GMT
USER kong
# Thu, 15 Jun 2023 06:25:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:25:15 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb51f944ac07d5786d81ea9e5223532bd0fc2724b596128d6c6bfb4622548e7`  
		Last Modified: Thu, 15 Jun 2023 06:26:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0ea639b18a7afef1350cd95f2c2c066cca2f54a3df6e97a7e86483e91566e9`  
		Last Modified: Thu, 15 Jun 2023 06:26:47 GMT  
		Size: 72.8 MB (72835718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63061c0a2f964430e9d29a86c8866f9b64a4d76c4102fb4508b66d2eb354f7d`  
		Last Modified: Thu, 15 Jun 2023 06:26:40 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:440179860d6592ac71ab2aa38baa3b43da04a46e1b8c398f46d23bc1298f8f66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73631302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66027ffeec8745797878c3e3898ddb0355ff120ecb2634833b84d17c22ece6d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:41:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 00:42:07 GMT
ARG KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 00:42:07 GMT
ENV KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 00:42:08 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Thu, 15 Jun 2023 00:42:08 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Thu, 15 Jun 2023 00:42:08 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 00:42:08 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:42:08 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 00:42:15 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 00:42:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:16 GMT
USER kong
# Thu, 15 Jun 2023 00:42:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:16 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940d9fed445e052edcf4526f82739dd13d3f896eee44d0e7f5ebee7ef05bcc3b`  
		Last Modified: Thu, 15 Jun 2023 00:43:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ef0525a80cd2df99acdab00fb0d3a3c1990e46f334a3a78d96509a5ba1535f`  
		Last Modified: Thu, 15 Jun 2023 00:43:17 GMT  
		Size: 70.9 MB (70922382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e236f022db4cf2d3a5525147f6383071ab5184218e5dcd71a4c6754190fdd8a`  
		Last Modified: Thu, 15 Jun 2023 00:43:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0-alpine`

```console
$ docker pull kong@sha256:c16f02938ab7ae019576dfc17a72e0408393b74ef5a363eb1d9f4d673bffa8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:dbdab62f9949e0843b7d8a46740b805940c6214a78bdab5bf61d169075affbc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75644403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cde42fd180357ec474d41db513f1f83b601663b89a41dedd1b04abb9543e8fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:24:51 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 06:25:05 GMT
ARG KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 06:25:05 GMT
ENV KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 06:25:05 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Thu, 15 Jun 2023 06:25:06 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Thu, 15 Jun 2023 06:25:06 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 06:25:06 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:25:06 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 06:25:14 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 06:25:14 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:25:14 GMT
USER kong
# Thu, 15 Jun 2023 06:25:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:25:15 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb51f944ac07d5786d81ea9e5223532bd0fc2724b596128d6c6bfb4622548e7`  
		Last Modified: Thu, 15 Jun 2023 06:26:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0ea639b18a7afef1350cd95f2c2c066cca2f54a3df6e97a7e86483e91566e9`  
		Last Modified: Thu, 15 Jun 2023 06:26:47 GMT  
		Size: 72.8 MB (72835718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63061c0a2f964430e9d29a86c8866f9b64a4d76c4102fb4508b66d2eb354f7d`  
		Last Modified: Thu, 15 Jun 2023 06:26:40 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:440179860d6592ac71ab2aa38baa3b43da04a46e1b8c398f46d23bc1298f8f66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73631302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66027ffeec8745797878c3e3898ddb0355ff120ecb2634833b84d17c22ece6d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:41:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 00:42:07 GMT
ARG KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 00:42:07 GMT
ENV KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 00:42:08 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Thu, 15 Jun 2023 00:42:08 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Thu, 15 Jun 2023 00:42:08 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 00:42:08 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:42:08 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 00:42:15 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 00:42:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:16 GMT
USER kong
# Thu, 15 Jun 2023 00:42:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:16 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940d9fed445e052edcf4526f82739dd13d3f896eee44d0e7f5ebee7ef05bcc3b`  
		Last Modified: Thu, 15 Jun 2023 00:43:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ef0525a80cd2df99acdab00fb0d3a3c1990e46f334a3a78d96509a5ba1535f`  
		Last Modified: Thu, 15 Jun 2023 00:43:17 GMT  
		Size: 70.9 MB (70922382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e236f022db4cf2d3a5525147f6383071ab5184218e5dcd71a4c6754190fdd8a`  
		Last Modified: Thu, 15 Jun 2023 00:43:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0-ubuntu`

```console
$ docker pull kong@sha256:738bdbd123ee7b0bed1f9038fa0bbc1beddc53ae8980dab6b64df135f24b2d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e9d5dda1bd4f39e7fa0e6bcf12718bfd1e1f4057db65fa53fd48096e4aa0fbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101694617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c7abb2de81c0557d2da44bf4acd75ec4ff518d832005295e87e3b132e0b032`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:48:57 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 18 Apr 2023 00:48:57 GMT
ARG ASSET=ce
# Tue, 18 Apr 2023 00:48:57 GMT
ENV ASSET=ce
# Tue, 18 Apr 2023 00:48:57 GMT
ARG EE_PORTS
# Tue, 18 Apr 2023 00:48:57 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Tue, 18 Apr 2023 00:49:32 GMT
ARG KONG_VERSION=3.0.2
# Tue, 18 Apr 2023 00:49:32 GMT
ENV KONG_VERSION=3.0.2
# Tue, 18 Apr 2023 00:49:32 GMT
ARG KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396
# Tue, 18 Apr 2023 00:49:32 GMT
ARG KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
# Tue, 18 Apr 2023 00:49:52 GMT
# ARGS: KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396 KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 18 Apr 2023 00:49:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 18 Apr 2023 00:49:53 GMT
USER kong
# Tue, 18 Apr 2023 00:49:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 00:49:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 18 Apr 2023 00:49:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Apr 2023 00:49:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 18 Apr 2023 00:49:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270117cfa3f1bf43891c96ffc5e3f48c9b1b960b8f1c17ad7d5cbb6971f0fbd`  
		Last Modified: Tue, 18 Apr 2023 00:50:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3e94b7778f468bc9687113229b1550d32f2d19632c324489f5d87c564f2749`  
		Last Modified: Tue, 18 Apr 2023 00:50:49 GMT  
		Size: 73.1 MB (73115045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3709def9dda22e3f52d5000041dd3ba80e64c58ca7e5ff6738b29dd2cedbf`  
		Last Modified: Tue, 18 Apr 2023 00:50:38 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:937d285da6fa08264c2c28e8e997ea4c87520d795f513d9966fe5d7f75a8fc32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98937255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb522eb11ee3d925d76914207df69726d88542c8ce5afc775b3300ed32a7df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:55:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 18 Apr 2023 01:55:38 GMT
ARG ASSET=ce
# Tue, 18 Apr 2023 01:55:38 GMT
ENV ASSET=ce
# Tue, 18 Apr 2023 01:55:38 GMT
ARG EE_PORTS
# Tue, 18 Apr 2023 01:55:38 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Tue, 18 Apr 2023 01:56:02 GMT
ARG KONG_VERSION=3.0.2
# Tue, 18 Apr 2023 01:56:02 GMT
ENV KONG_VERSION=3.0.2
# Tue, 18 Apr 2023 01:56:02 GMT
ARG KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396
# Tue, 18 Apr 2023 01:56:02 GMT
ARG KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
# Tue, 18 Apr 2023 01:56:22 GMT
# ARGS: KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396 KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 18 Apr 2023 01:56:23 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 18 Apr 2023 01:56:23 GMT
USER kong
# Tue, 18 Apr 2023 01:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 01:56:23 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 18 Apr 2023 01:56:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Apr 2023 01:56:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 18 Apr 2023 01:56:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33117919705427cc2b91c73428239666db66c5521aad5bb7169b1d6fc9d0b5dc`  
		Last Modified: Tue, 18 Apr 2023 01:56:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5d517b7ce411115a69d3a88946c56ca87258d1cd048d9a878b949d8a2abb5`  
		Last Modified: Tue, 18 Apr 2023 01:57:08 GMT  
		Size: 71.7 MB (71739854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e1a10cf887d91c6182976d4bbbb1e0b2c85d8ed10c3e11373e94c35e6dbdc9`  
		Last Modified: Tue, 18 Apr 2023 01:56:59 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.2`

```console
$ docker pull kong@sha256:c16f02938ab7ae019576dfc17a72e0408393b74ef5a363eb1d9f4d673bffa8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.2` - linux; amd64

```console
$ docker pull kong@sha256:dbdab62f9949e0843b7d8a46740b805940c6214a78bdab5bf61d169075affbc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75644403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cde42fd180357ec474d41db513f1f83b601663b89a41dedd1b04abb9543e8fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:24:51 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 06:25:05 GMT
ARG KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 06:25:05 GMT
ENV KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 06:25:05 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Thu, 15 Jun 2023 06:25:06 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Thu, 15 Jun 2023 06:25:06 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 06:25:06 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:25:06 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 06:25:14 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 06:25:14 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:25:14 GMT
USER kong
# Thu, 15 Jun 2023 06:25:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:25:15 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb51f944ac07d5786d81ea9e5223532bd0fc2724b596128d6c6bfb4622548e7`  
		Last Modified: Thu, 15 Jun 2023 06:26:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0ea639b18a7afef1350cd95f2c2c066cca2f54a3df6e97a7e86483e91566e9`  
		Last Modified: Thu, 15 Jun 2023 06:26:47 GMT  
		Size: 72.8 MB (72835718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63061c0a2f964430e9d29a86c8866f9b64a4d76c4102fb4508b66d2eb354f7d`  
		Last Modified: Thu, 15 Jun 2023 06:26:40 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:440179860d6592ac71ab2aa38baa3b43da04a46e1b8c398f46d23bc1298f8f66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73631302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66027ffeec8745797878c3e3898ddb0355ff120ecb2634833b84d17c22ece6d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:41:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 00:42:07 GMT
ARG KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 00:42:07 GMT
ENV KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 00:42:08 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Thu, 15 Jun 2023 00:42:08 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Thu, 15 Jun 2023 00:42:08 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 00:42:08 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:42:08 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 00:42:15 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 00:42:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:16 GMT
USER kong
# Thu, 15 Jun 2023 00:42:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:16 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940d9fed445e052edcf4526f82739dd13d3f896eee44d0e7f5ebee7ef05bcc3b`  
		Last Modified: Thu, 15 Jun 2023 00:43:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ef0525a80cd2df99acdab00fb0d3a3c1990e46f334a3a78d96509a5ba1535f`  
		Last Modified: Thu, 15 Jun 2023 00:43:17 GMT  
		Size: 70.9 MB (70922382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e236f022db4cf2d3a5525147f6383071ab5184218e5dcd71a4c6754190fdd8a`  
		Last Modified: Thu, 15 Jun 2023 00:43:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.2-alpine`

```console
$ docker pull kong@sha256:c16f02938ab7ae019576dfc17a72e0408393b74ef5a363eb1d9f4d673bffa8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:dbdab62f9949e0843b7d8a46740b805940c6214a78bdab5bf61d169075affbc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75644403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cde42fd180357ec474d41db513f1f83b601663b89a41dedd1b04abb9543e8fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:24:51 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 06:25:05 GMT
ARG KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 06:25:05 GMT
ENV KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 06:25:05 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Thu, 15 Jun 2023 06:25:06 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Thu, 15 Jun 2023 06:25:06 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 06:25:06 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:25:06 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 06:25:14 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 06:25:14 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:25:14 GMT
USER kong
# Thu, 15 Jun 2023 06:25:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:25:15 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb51f944ac07d5786d81ea9e5223532bd0fc2724b596128d6c6bfb4622548e7`  
		Last Modified: Thu, 15 Jun 2023 06:26:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0ea639b18a7afef1350cd95f2c2c066cca2f54a3df6e97a7e86483e91566e9`  
		Last Modified: Thu, 15 Jun 2023 06:26:47 GMT  
		Size: 72.8 MB (72835718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63061c0a2f964430e9d29a86c8866f9b64a4d76c4102fb4508b66d2eb354f7d`  
		Last Modified: Thu, 15 Jun 2023 06:26:40 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:440179860d6592ac71ab2aa38baa3b43da04a46e1b8c398f46d23bc1298f8f66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73631302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66027ffeec8745797878c3e3898ddb0355ff120ecb2634833b84d17c22ece6d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:41:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 00:42:07 GMT
ARG KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 00:42:07 GMT
ENV KONG_VERSION=3.0.2
# Thu, 15 Jun 2023 00:42:08 GMT
ARG KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e
# Thu, 15 Jun 2023 00:42:08 GMT
ARG KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
# Thu, 15 Jun 2023 00:42:08 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 00:42:08 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:42:08 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 00:42:15 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=5f2f4c953cfc06c750614148b90f8216321b869ba44e1cf509f2dbbd9182516e KONG_ARM64_SHA=049efeb9f82898a0c4b0e3257c3389a2cb8fbf51339b497cff78c2687106718b
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 00:42:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:16 GMT
USER kong
# Thu, 15 Jun 2023 00:42:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:16 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940d9fed445e052edcf4526f82739dd13d3f896eee44d0e7f5ebee7ef05bcc3b`  
		Last Modified: Thu, 15 Jun 2023 00:43:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ef0525a80cd2df99acdab00fb0d3a3c1990e46f334a3a78d96509a5ba1535f`  
		Last Modified: Thu, 15 Jun 2023 00:43:17 GMT  
		Size: 70.9 MB (70922382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e236f022db4cf2d3a5525147f6383071ab5184218e5dcd71a4c6754190fdd8a`  
		Last Modified: Thu, 15 Jun 2023 00:43:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.0.2-ubuntu`

```console
$ docker pull kong@sha256:738bdbd123ee7b0bed1f9038fa0bbc1beddc53ae8980dab6b64df135f24b2d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.0.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e9d5dda1bd4f39e7fa0e6bcf12718bfd1e1f4057db65fa53fd48096e4aa0fbe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101694617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c7abb2de81c0557d2da44bf4acd75ec4ff518d832005295e87e3b132e0b032`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:48:57 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 18 Apr 2023 00:48:57 GMT
ARG ASSET=ce
# Tue, 18 Apr 2023 00:48:57 GMT
ENV ASSET=ce
# Tue, 18 Apr 2023 00:48:57 GMT
ARG EE_PORTS
# Tue, 18 Apr 2023 00:48:57 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Tue, 18 Apr 2023 00:49:32 GMT
ARG KONG_VERSION=3.0.2
# Tue, 18 Apr 2023 00:49:32 GMT
ENV KONG_VERSION=3.0.2
# Tue, 18 Apr 2023 00:49:32 GMT
ARG KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396
# Tue, 18 Apr 2023 00:49:32 GMT
ARG KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
# Tue, 18 Apr 2023 00:49:52 GMT
# ARGS: KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396 KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 18 Apr 2023 00:49:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 18 Apr 2023 00:49:53 GMT
USER kong
# Tue, 18 Apr 2023 00:49:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 00:49:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 18 Apr 2023 00:49:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Apr 2023 00:49:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 18 Apr 2023 00:49:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270117cfa3f1bf43891c96ffc5e3f48c9b1b960b8f1c17ad7d5cbb6971f0fbd`  
		Last Modified: Tue, 18 Apr 2023 00:50:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3e94b7778f468bc9687113229b1550d32f2d19632c324489f5d87c564f2749`  
		Last Modified: Tue, 18 Apr 2023 00:50:49 GMT  
		Size: 73.1 MB (73115045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3709def9dda22e3f52d5000041dd3ba80e64c58ca7e5ff6738b29dd2cedbf`  
		Last Modified: Tue, 18 Apr 2023 00:50:38 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.0.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:937d285da6fa08264c2c28e8e997ea4c87520d795f513d9966fe5d7f75a8fc32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98937255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb522eb11ee3d925d76914207df69726d88542c8ce5afc775b3300ed32a7df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:55:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 18 Apr 2023 01:55:38 GMT
ARG ASSET=ce
# Tue, 18 Apr 2023 01:55:38 GMT
ENV ASSET=ce
# Tue, 18 Apr 2023 01:55:38 GMT
ARG EE_PORTS
# Tue, 18 Apr 2023 01:55:38 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Tue, 18 Apr 2023 01:56:02 GMT
ARG KONG_VERSION=3.0.2
# Tue, 18 Apr 2023 01:56:02 GMT
ENV KONG_VERSION=3.0.2
# Tue, 18 Apr 2023 01:56:02 GMT
ARG KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396
# Tue, 18 Apr 2023 01:56:02 GMT
ARG KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
# Tue, 18 Apr 2023 01:56:22 GMT
# ARGS: KONG_AMD64_SHA=ad9b0b97b48e2a939d2aefa1ae2e4f2924a4cda5382e99524589ccbb90f7c396 KONG_ARM64_SHA=8e10e6693ece4166c9acf3eb0745c119468d6902e7c27b2841f900644b3e2c53
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 18 Apr 2023 01:56:23 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 18 Apr 2023 01:56:23 GMT
USER kong
# Tue, 18 Apr 2023 01:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 01:56:23 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 18 Apr 2023 01:56:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Apr 2023 01:56:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 18 Apr 2023 01:56:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33117919705427cc2b91c73428239666db66c5521aad5bb7169b1d6fc9d0b5dc`  
		Last Modified: Tue, 18 Apr 2023 01:56:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5d517b7ce411115a69d3a88946c56ca87258d1cd048d9a878b949d8a2abb5`  
		Last Modified: Tue, 18 Apr 2023 01:57:08 GMT  
		Size: 71.7 MB (71739854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e1a10cf887d91c6182976d4bbbb1e0b2c85d8ed10c3e11373e94c35e6dbdc9`  
		Last Modified: Tue, 18 Apr 2023 01:56:59 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1`

```console
$ docker pull kong@sha256:f8a5fbd18b2aa19765201e26c1104def41a8ec6177a80840939307062270fbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1` - linux; amd64

```console
$ docker pull kong@sha256:69b75ed0bdb6ba6e81d90d2aedcab947d67f9565644d64fc112b56cdc1500d97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75688911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8929f3c41e7e38ceda54c16364709ce8fa22846a410d5eb933ce5bd8d1d4966`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:24:51 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 06:24:51 GMT
ARG KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 06:24:51 GMT
ENV KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 06:24:52 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Thu, 15 Jun 2023 06:24:52 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Thu, 15 Jun 2023 06:24:52 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 06:24:52 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:24:52 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 06:24:59 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 06:24:59 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:24:59 GMT
USER kong
# Thu, 15 Jun 2023 06:24:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:24:59 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cc8882a14901bbac226d538a5a1189bc09c6051ce266e3796316d2fd5c06b`  
		Last Modified: Thu, 15 Jun 2023 06:26:20 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d89016896ec2b5175ddfe42106245e95d33efcd4521f46d7eaebb0ad30f13`  
		Last Modified: Thu, 15 Jun 2023 06:26:28 GMT  
		Size: 72.9 MB (72880224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46f4698ce39118443bf7df323b3355fc755e901a7217156d40f920f5297fada`  
		Last Modified: Thu, 15 Jun 2023 06:26:20 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:23d3a20180d1bf763ad7360b7c9ed51d222953736b5d672ddc4921dba8daab74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73704647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be03fcbc57b0bccedc31292d3be6d1c56896251b5aebf0a86f74fe3bf8a1ed1b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:41:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 00:41:55 GMT
ARG KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 00:41:55 GMT
ENV KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 00:41:55 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Thu, 15 Jun 2023 00:41:55 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Thu, 15 Jun 2023 00:41:55 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 00:41:55 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:41:55 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 00:42:02 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 00:42:02 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:02 GMT
USER kong
# Thu, 15 Jun 2023 00:42:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:03 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:03 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e3e57ed4acbf2d9f596b31a20c6341d8172233d7291253d484be6a57df0c9f`  
		Last Modified: Thu, 15 Jun 2023 00:42:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e50a11265ca59622b21c480195c8d6017270abaa14e97d0ba2db719a8364f4e`  
		Last Modified: Thu, 15 Jun 2023 00:42:59 GMT  
		Size: 71.0 MB (70995728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497a79f5e6a72fce6df0f2ec91f63cce422cdd5e233cb3889cb83127d0c9effc`  
		Last Modified: Thu, 15 Jun 2023 00:42:52 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1-ubuntu`

```console
$ docker pull kong@sha256:3bde6e63802d1c6799673d86602bc18a0ad7df02a928a980163360699b9283a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:fb7def9d63b24dc4c240b345e7e9355337786d632661945e06a15ef20e4779a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101731018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5498f3ffdb5118b22860bb4093d18caa5b3149307152c58abc431e05d8685579`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:48:57 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 18 Apr 2023 00:48:57 GMT
ARG ASSET=ce
# Tue, 18 Apr 2023 00:48:57 GMT
ENV ASSET=ce
# Tue, 18 Apr 2023 00:48:57 GMT
ARG EE_PORTS
# Tue, 18 Apr 2023 00:48:57 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Tue, 18 Apr 2023 00:48:57 GMT
ARG KONG_VERSION=3.1.1
# Tue, 18 Apr 2023 00:48:57 GMT
ENV KONG_VERSION=3.1.1
# Tue, 18 Apr 2023 00:48:57 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Tue, 18 Apr 2023 00:48:57 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Tue, 18 Apr 2023 00:49:26 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 18 Apr 2023 00:49:26 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 18 Apr 2023 00:49:26 GMT
USER kong
# Tue, 18 Apr 2023 00:49:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 00:49:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 18 Apr 2023 00:49:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Apr 2023 00:49:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 18 Apr 2023 00:49:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270117cfa3f1bf43891c96ffc5e3f48c9b1b960b8f1c17ad7d5cbb6971f0fbd`  
		Last Modified: Tue, 18 Apr 2023 00:50:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccee49244e3687399c9c24cc0ce516b0905e7442ed02f0fe26a5a84f5538a7b`  
		Last Modified: Tue, 18 Apr 2023 00:50:28 GMT  
		Size: 73.2 MB (73151444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53853e3583dd41f1e3da5406c276e344418ddaae1e4dbe056f2e4e205734273e`  
		Last Modified: Tue, 18 Apr 2023 00:50:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c5b08a0c6e5170deba532287fe325be7b87ecb0c4710b857c519ae68507091ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98969390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85eab6242a1c3c38ed07152b648ebef2d657a39b9699ea9fb23dd60a94dc1a78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:55:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 18 Apr 2023 01:55:38 GMT
ARG ASSET=ce
# Tue, 18 Apr 2023 01:55:38 GMT
ENV ASSET=ce
# Tue, 18 Apr 2023 01:55:38 GMT
ARG EE_PORTS
# Tue, 18 Apr 2023 01:55:38 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Tue, 18 Apr 2023 01:55:39 GMT
ARG KONG_VERSION=3.1.1
# Tue, 18 Apr 2023 01:55:39 GMT
ENV KONG_VERSION=3.1.1
# Tue, 18 Apr 2023 01:55:39 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Tue, 18 Apr 2023 01:55:39 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Tue, 18 Apr 2023 01:55:55 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 18 Apr 2023 01:55:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 18 Apr 2023 01:55:56 GMT
USER kong
# Tue, 18 Apr 2023 01:55:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 01:55:57 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 18 Apr 2023 01:55:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Apr 2023 01:55:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 18 Apr 2023 01:55:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33117919705427cc2b91c73428239666db66c5521aad5bb7169b1d6fc9d0b5dc`  
		Last Modified: Tue, 18 Apr 2023 01:56:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd8eef4dc95b72b5204ea83b481f2af54e5c5c4cf27232918bfcccd5cafd2c5`  
		Last Modified: Tue, 18 Apr 2023 01:56:50 GMT  
		Size: 71.8 MB (71771988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83592683ff2a59bc4dc1fb9e4c1df9fcd9e9cf7c783c57043f79f67657a7daab`  
		Last Modified: Tue, 18 Apr 2023 01:56:41 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1`

```console
$ docker pull kong@sha256:f8a5fbd18b2aa19765201e26c1104def41a8ec6177a80840939307062270fbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1` - linux; amd64

```console
$ docker pull kong@sha256:69b75ed0bdb6ba6e81d90d2aedcab947d67f9565644d64fc112b56cdc1500d97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75688911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8929f3c41e7e38ceda54c16364709ce8fa22846a410d5eb933ce5bd8d1d4966`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:24:51 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 06:24:51 GMT
ARG KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 06:24:51 GMT
ENV KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 06:24:52 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Thu, 15 Jun 2023 06:24:52 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Thu, 15 Jun 2023 06:24:52 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 06:24:52 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:24:52 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 06:24:59 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 06:24:59 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:24:59 GMT
USER kong
# Thu, 15 Jun 2023 06:24:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:24:59 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cc8882a14901bbac226d538a5a1189bc09c6051ce266e3796316d2fd5c06b`  
		Last Modified: Thu, 15 Jun 2023 06:26:20 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d89016896ec2b5175ddfe42106245e95d33efcd4521f46d7eaebb0ad30f13`  
		Last Modified: Thu, 15 Jun 2023 06:26:28 GMT  
		Size: 72.9 MB (72880224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46f4698ce39118443bf7df323b3355fc755e901a7217156d40f920f5297fada`  
		Last Modified: Thu, 15 Jun 2023 06:26:20 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:23d3a20180d1bf763ad7360b7c9ed51d222953736b5d672ddc4921dba8daab74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73704647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be03fcbc57b0bccedc31292d3be6d1c56896251b5aebf0a86f74fe3bf8a1ed1b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:41:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 00:41:55 GMT
ARG KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 00:41:55 GMT
ENV KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 00:41:55 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Thu, 15 Jun 2023 00:41:55 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Thu, 15 Jun 2023 00:41:55 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 00:41:55 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:41:55 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 00:42:02 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 00:42:02 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:02 GMT
USER kong
# Thu, 15 Jun 2023 00:42:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:03 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:03 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e3e57ed4acbf2d9f596b31a20c6341d8172233d7291253d484be6a57df0c9f`  
		Last Modified: Thu, 15 Jun 2023 00:42:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e50a11265ca59622b21c480195c8d6017270abaa14e97d0ba2db719a8364f4e`  
		Last Modified: Thu, 15 Jun 2023 00:42:59 GMT  
		Size: 71.0 MB (70995728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497a79f5e6a72fce6df0f2ec91f63cce422cdd5e233cb3889cb83127d0c9effc`  
		Last Modified: Thu, 15 Jun 2023 00:42:52 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1-alpine`

```console
$ docker pull kong@sha256:f8a5fbd18b2aa19765201e26c1104def41a8ec6177a80840939307062270fbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:69b75ed0bdb6ba6e81d90d2aedcab947d67f9565644d64fc112b56cdc1500d97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75688911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8929f3c41e7e38ceda54c16364709ce8fa22846a410d5eb933ce5bd8d1d4966`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:24:51 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 06:24:51 GMT
ARG KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 06:24:51 GMT
ENV KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 06:24:52 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Thu, 15 Jun 2023 06:24:52 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Thu, 15 Jun 2023 06:24:52 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 06:24:52 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:24:52 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 06:24:59 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 06:24:59 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:24:59 GMT
USER kong
# Thu, 15 Jun 2023 06:24:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:24:59 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:25:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:25:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:25:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cc8882a14901bbac226d538a5a1189bc09c6051ce266e3796316d2fd5c06b`  
		Last Modified: Thu, 15 Jun 2023 06:26:20 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d89016896ec2b5175ddfe42106245e95d33efcd4521f46d7eaebb0ad30f13`  
		Last Modified: Thu, 15 Jun 2023 06:26:28 GMT  
		Size: 72.9 MB (72880224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46f4698ce39118443bf7df323b3355fc755e901a7217156d40f920f5297fada`  
		Last Modified: Thu, 15 Jun 2023 06:26:20 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:23d3a20180d1bf763ad7360b7c9ed51d222953736b5d672ddc4921dba8daab74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73704647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be03fcbc57b0bccedc31292d3be6d1c56896251b5aebf0a86f74fe3bf8a1ed1b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:41:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 00:41:55 GMT
ARG KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 00:41:55 GMT
ENV KONG_VERSION=3.1.1
# Thu, 15 Jun 2023 00:41:55 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Thu, 15 Jun 2023 00:41:55 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Thu, 15 Jun 2023 00:41:55 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 00:41:55 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 00:41:55 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 00:42:02 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 00:42:02 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 00:42:02 GMT
USER kong
# Thu, 15 Jun 2023 00:42:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:42:03 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 00:42:03 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 00:42:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 00:42:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e3e57ed4acbf2d9f596b31a20c6341d8172233d7291253d484be6a57df0c9f`  
		Last Modified: Thu, 15 Jun 2023 00:42:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e50a11265ca59622b21c480195c8d6017270abaa14e97d0ba2db719a8364f4e`  
		Last Modified: Thu, 15 Jun 2023 00:42:59 GMT  
		Size: 71.0 MB (70995728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497a79f5e6a72fce6df0f2ec91f63cce422cdd5e233cb3889cb83127d0c9effc`  
		Last Modified: Thu, 15 Jun 2023 00:42:52 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1-ubuntu`

```console
$ docker pull kong@sha256:3bde6e63802d1c6799673d86602bc18a0ad7df02a928a980163360699b9283a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:fb7def9d63b24dc4c240b345e7e9355337786d632661945e06a15ef20e4779a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101731018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5498f3ffdb5118b22860bb4093d18caa5b3149307152c58abc431e05d8685579`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:48:57 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 18 Apr 2023 00:48:57 GMT
ARG ASSET=ce
# Tue, 18 Apr 2023 00:48:57 GMT
ENV ASSET=ce
# Tue, 18 Apr 2023 00:48:57 GMT
ARG EE_PORTS
# Tue, 18 Apr 2023 00:48:57 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Tue, 18 Apr 2023 00:48:57 GMT
ARG KONG_VERSION=3.1.1
# Tue, 18 Apr 2023 00:48:57 GMT
ENV KONG_VERSION=3.1.1
# Tue, 18 Apr 2023 00:48:57 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Tue, 18 Apr 2023 00:48:57 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Tue, 18 Apr 2023 00:49:26 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 18 Apr 2023 00:49:26 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 18 Apr 2023 00:49:26 GMT
USER kong
# Tue, 18 Apr 2023 00:49:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 00:49:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 18 Apr 2023 00:49:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Apr 2023 00:49:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 18 Apr 2023 00:49:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270117cfa3f1bf43891c96ffc5e3f48c9b1b960b8f1c17ad7d5cbb6971f0fbd`  
		Last Modified: Tue, 18 Apr 2023 00:50:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccee49244e3687399c9c24cc0ce516b0905e7442ed02f0fe26a5a84f5538a7b`  
		Last Modified: Tue, 18 Apr 2023 00:50:28 GMT  
		Size: 73.2 MB (73151444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53853e3583dd41f1e3da5406c276e344418ddaae1e4dbe056f2e4e205734273e`  
		Last Modified: Tue, 18 Apr 2023 00:50:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c5b08a0c6e5170deba532287fe325be7b87ecb0c4710b857c519ae68507091ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98969390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85eab6242a1c3c38ed07152b648ebef2d657a39b9699ea9fb23dd60a94dc1a78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:55:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 18 Apr 2023 01:55:38 GMT
ARG ASSET=ce
# Tue, 18 Apr 2023 01:55:38 GMT
ENV ASSET=ce
# Tue, 18 Apr 2023 01:55:38 GMT
ARG EE_PORTS
# Tue, 18 Apr 2023 01:55:38 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Tue, 18 Apr 2023 01:55:39 GMT
ARG KONG_VERSION=3.1.1
# Tue, 18 Apr 2023 01:55:39 GMT
ENV KONG_VERSION=3.1.1
# Tue, 18 Apr 2023 01:55:39 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Tue, 18 Apr 2023 01:55:39 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Tue, 18 Apr 2023 01:55:55 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 18 Apr 2023 01:55:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 18 Apr 2023 01:55:56 GMT
USER kong
# Tue, 18 Apr 2023 01:55:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 01:55:57 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 18 Apr 2023 01:55:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Apr 2023 01:55:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 18 Apr 2023 01:55:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33117919705427cc2b91c73428239666db66c5521aad5bb7169b1d6fc9d0b5dc`  
		Last Modified: Tue, 18 Apr 2023 01:56:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd8eef4dc95b72b5204ea83b481f2af54e5c5c4cf27232918bfcccd5cafd2c5`  
		Last Modified: Tue, 18 Apr 2023 01:56:50 GMT  
		Size: 71.8 MB (71771988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83592683ff2a59bc4dc1fb9e4c1df9fcd9e9cf7c783c57043f79f67657a7daab`  
		Last Modified: Tue, 18 Apr 2023 01:56:41 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2`

```console
$ docker pull kong@sha256:52782bc0845e9d2d3614bcf10a4a2aaa8c0bdd3be3c5ced47dd69a66358be14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2` - linux; amd64

```console
$ docker pull kong@sha256:1c4691ad9035578596df51c02b3a217f608caf064882c052303bdc71a2201000
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d8fa7840717c8a6c36e3a0c706efc27125d6109696f69ccea4481444c64996`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Jun 2023 01:31:51 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Jun 2023 01:32:08 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:32:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:32:09 GMT
USER kong
# Fri, 02 Jun 2023 01:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:32:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:32:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3db4ca5fc9b41cfe22f46359c98c0c8bdb31af75d14d49d6cbfd6efc72de74`  
		Last Modified: Fri, 02 Jun 2023 01:33:47 GMT  
		Size: 44.0 MB (44024732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eef354f6811f9cbf79e43146c2d557c005b8ec89a2559fd734618df265a177f`  
		Last Modified: Fri, 02 Jun 2023 01:33:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:31c9b5b768fb7781bda9447b5d431bd1d599afecd78593b5444181095cfe442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78577563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bdbfd1aa2831d669e406b1c3a43b3c32edc014496f733213359e0dc51e96db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_VERSION=3.2.2
# Thu, 01 Jun 2023 23:38:27 GMT
ENV KONG_VERSION=3.2.2
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Thu, 01 Jun 2023 23:38:43 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:43 GMT
USER kong
# Thu, 01 Jun 2023 23:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:43 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4588fe378cf817911be63e15830cf5753f8c9471c3704b27917672562f2aef8`  
		Last Modified: Thu, 01 Jun 2023 23:40:15 GMT  
		Size: 50.2 MB (50187238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b4d9fba2f36ddae4007adf8e912cd58ecceab0c29b27fe1c0ecaaf2fc8ff2`  
		Last Modified: Thu, 01 Jun 2023 23:40:08 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2-ubuntu`

```console
$ docker pull kong@sha256:52782bc0845e9d2d3614bcf10a4a2aaa8c0bdd3be3c5ced47dd69a66358be14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1c4691ad9035578596df51c02b3a217f608caf064882c052303bdc71a2201000
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d8fa7840717c8a6c36e3a0c706efc27125d6109696f69ccea4481444c64996`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Jun 2023 01:31:51 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Jun 2023 01:32:08 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:32:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:32:09 GMT
USER kong
# Fri, 02 Jun 2023 01:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:32:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:32:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3db4ca5fc9b41cfe22f46359c98c0c8bdb31af75d14d49d6cbfd6efc72de74`  
		Last Modified: Fri, 02 Jun 2023 01:33:47 GMT  
		Size: 44.0 MB (44024732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eef354f6811f9cbf79e43146c2d557c005b8ec89a2559fd734618df265a177f`  
		Last Modified: Fri, 02 Jun 2023 01:33:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:31c9b5b768fb7781bda9447b5d431bd1d599afecd78593b5444181095cfe442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78577563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bdbfd1aa2831d669e406b1c3a43b3c32edc014496f733213359e0dc51e96db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_VERSION=3.2.2
# Thu, 01 Jun 2023 23:38:27 GMT
ENV KONG_VERSION=3.2.2
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Thu, 01 Jun 2023 23:38:43 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:43 GMT
USER kong
# Thu, 01 Jun 2023 23:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:43 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4588fe378cf817911be63e15830cf5753f8c9471c3704b27917672562f2aef8`  
		Last Modified: Thu, 01 Jun 2023 23:40:15 GMT  
		Size: 50.2 MB (50187238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b4d9fba2f36ddae4007adf8e912cd58ecceab0c29b27fe1c0ecaaf2fc8ff2`  
		Last Modified: Thu, 01 Jun 2023 23:40:08 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2.2`

```console
$ docker pull kong@sha256:52782bc0845e9d2d3614bcf10a4a2aaa8c0bdd3be3c5ced47dd69a66358be14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2.2` - linux; amd64

```console
$ docker pull kong@sha256:1c4691ad9035578596df51c02b3a217f608caf064882c052303bdc71a2201000
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d8fa7840717c8a6c36e3a0c706efc27125d6109696f69ccea4481444c64996`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Jun 2023 01:31:51 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Jun 2023 01:32:08 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:32:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:32:09 GMT
USER kong
# Fri, 02 Jun 2023 01:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:32:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:32:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3db4ca5fc9b41cfe22f46359c98c0c8bdb31af75d14d49d6cbfd6efc72de74`  
		Last Modified: Fri, 02 Jun 2023 01:33:47 GMT  
		Size: 44.0 MB (44024732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eef354f6811f9cbf79e43146c2d557c005b8ec89a2559fd734618df265a177f`  
		Last Modified: Fri, 02 Jun 2023 01:33:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:31c9b5b768fb7781bda9447b5d431bd1d599afecd78593b5444181095cfe442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78577563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bdbfd1aa2831d669e406b1c3a43b3c32edc014496f733213359e0dc51e96db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_VERSION=3.2.2
# Thu, 01 Jun 2023 23:38:27 GMT
ENV KONG_VERSION=3.2.2
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Thu, 01 Jun 2023 23:38:43 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:43 GMT
USER kong
# Thu, 01 Jun 2023 23:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:43 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4588fe378cf817911be63e15830cf5753f8c9471c3704b27917672562f2aef8`  
		Last Modified: Thu, 01 Jun 2023 23:40:15 GMT  
		Size: 50.2 MB (50187238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b4d9fba2f36ddae4007adf8e912cd58ecceab0c29b27fe1c0ecaaf2fc8ff2`  
		Last Modified: Thu, 01 Jun 2023 23:40:08 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2.2-alpine`

```console
$ docker pull kong@sha256:f985adcc9ed18baa749e0601ab373795579d2cbb23d982cd5bd14eb30adcdca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:3.2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:6c508876f692c8df3346e63119e36ac1a237384c8c44f02fefcb2b74cea99f36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36925700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96642dab3c1c86110eb73e5d6013381cf90df6c6dd50c5295ea3fb7cd1f0a08f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:24:27 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jun 2023 06:24:39 GMT
ARG KONG_VERSION=3.2.2
# Thu, 15 Jun 2023 06:24:39 GMT
ENV KONG_VERSION=3.2.2
# Thu, 15 Jun 2023 06:24:39 GMT
ARG KONG_SHA256=a07c3bc0307e2d8fe33acb8be5fe659f348279540eaa267bc6968005094835ef
# Thu, 15 Jun 2023 06:24:40 GMT
ARG KONG_PREFIX=/usr/local/kong
# Thu, 15 Jun 2023 06:24:40 GMT
ENV KONG_PREFIX=/usr/local/kong
# Thu, 15 Jun 2023 06:24:40 GMT
ARG ASSET=remote
# Thu, 15 Jun 2023 06:24:40 GMT
ARG EE_PORTS
# Thu, 15 Jun 2023 06:24:40 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 15 Jun 2023 06:24:46 GMT
# ARGS: ASSET=remote KONG_SHA256=a07c3bc0307e2d8fe33acb8be5fe659f348279540eaa267bc6968005094835ef
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 15 Jun 2023 06:24:47 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 15 Jun 2023 06:24:47 GMT
USER kong
# Thu, 15 Jun 2023 06:24:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:24:47 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 15 Jun 2023 06:24:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:24:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Thu, 15 Jun 2023 06:24:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd039fb5ac2e17d182f72cb499825604a85321aa36a51fbdbb3f9fc226d114a9`  
		Last Modified: Thu, 15 Jun 2023 06:26:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef7ad483e17ea0283b93716e78b8f3397f1b187880b68963b0e7e5db7753481`  
		Last Modified: Thu, 15 Jun 2023 06:26:13 GMT  
		Size: 33.5 MB (33549698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ee442fb6c11d14c18f89e7c6d930d5c62b13d91a5a2af2fb628c49554b44b0`  
		Last Modified: Thu, 15 Jun 2023 06:26:08 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2.2-ubuntu`

```console
$ docker pull kong@sha256:52782bc0845e9d2d3614bcf10a4a2aaa8c0bdd3be3c5ced47dd69a66358be14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1c4691ad9035578596df51c02b3a217f608caf064882c052303bdc71a2201000
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d8fa7840717c8a6c36e3a0c706efc27125d6109696f69ccea4481444c64996`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Jun 2023 01:31:51 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Jun 2023 01:31:51 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Jun 2023 01:32:08 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:32:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:32:09 GMT
USER kong
# Fri, 02 Jun 2023 01:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:32:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:32:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3db4ca5fc9b41cfe22f46359c98c0c8bdb31af75d14d49d6cbfd6efc72de74`  
		Last Modified: Fri, 02 Jun 2023 01:33:47 GMT  
		Size: 44.0 MB (44024732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eef354f6811f9cbf79e43146c2d557c005b8ec89a2559fd734618df265a177f`  
		Last Modified: Fri, 02 Jun 2023 01:33:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:31c9b5b768fb7781bda9447b5d431bd1d599afecd78593b5444181095cfe442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78577563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bdbfd1aa2831d669e406b1c3a43b3c32edc014496f733213359e0dc51e96db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_VERSION=3.2.2
# Thu, 01 Jun 2023 23:38:27 GMT
ENV KONG_VERSION=3.2.2
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Thu, 01 Jun 2023 23:38:27 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Thu, 01 Jun 2023 23:38:43 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:43 GMT
USER kong
# Thu, 01 Jun 2023 23:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:43 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4588fe378cf817911be63e15830cf5753f8c9471c3704b27917672562f2aef8`  
		Last Modified: Thu, 01 Jun 2023 23:40:15 GMT  
		Size: 50.2 MB (50187238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b4d9fba2f36ddae4007adf8e912cd58ecceab0c29b27fe1c0ecaaf2fc8ff2`  
		Last Modified: Thu, 01 Jun 2023 23:40:08 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3`

```console
$ docker pull kong@sha256:9078cc4badc63e1b591ee5e8f1cd97d8a0659b7c783f5fdeeba77e0c6c78e5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3` - linux; amd64

```console
$ docker pull kong@sha256:cb97b3b9bd4540d09f246f855be72a044b342bbf980c96a0b8117b2700c98ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81311313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5971887ac84cdc4ba0a9c21b9212a6b94d1970e3664b1282ebc11b1954facf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:08 GMT
ARG KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ENV KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Fri, 02 Jun 2023 01:31:42 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:31:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:31:43 GMT
USER kong
# Fri, 02 Jun 2023 01:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:31:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:31:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:31:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:31:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8937d2707ca171dddcc194356d4edef593341b55286e3b54343d1bb304f2c023`  
		Last Modified: Fri, 02 Jun 2023 01:33:24 GMT  
		Size: 50.9 MB (50879757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c105bdc14980907cff3f5de1391848b1ca553a71da5d26d71345454e918caa`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:53f32385a7bb5533c03d3dba190cb1e257b0dfd46a41f6576b0b1fd91245d0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75728888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdec04b213ff81ba8f4c88338767b36a7a4c9f8f3c61d9dbe590be96fb51491`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ENV KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Thu, 01 Jun 2023 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:25 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:25 GMT
USER kong
# Thu, 01 Jun 2023 23:38:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a99a85577e3756d8a7bd71326e7a8674934ddb169bd5a4349103e197a58f983`  
		Last Modified: Thu, 01 Jun 2023 23:39:52 GMT  
		Size: 47.3 MB (47338562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e0e212694b9b9de8b4bcbb4713dbb848f27b1198ac68df26605d26d233870c`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3-ubuntu`

```console
$ docker pull kong@sha256:9078cc4badc63e1b591ee5e8f1cd97d8a0659b7c783f5fdeeba77e0c6c78e5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:cb97b3b9bd4540d09f246f855be72a044b342bbf980c96a0b8117b2700c98ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81311313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5971887ac84cdc4ba0a9c21b9212a6b94d1970e3664b1282ebc11b1954facf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:08 GMT
ARG KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ENV KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Fri, 02 Jun 2023 01:31:42 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:31:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:31:43 GMT
USER kong
# Fri, 02 Jun 2023 01:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:31:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:31:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:31:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:31:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8937d2707ca171dddcc194356d4edef593341b55286e3b54343d1bb304f2c023`  
		Last Modified: Fri, 02 Jun 2023 01:33:24 GMT  
		Size: 50.9 MB (50879757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c105bdc14980907cff3f5de1391848b1ca553a71da5d26d71345454e918caa`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:53f32385a7bb5533c03d3dba190cb1e257b0dfd46a41f6576b0b1fd91245d0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75728888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdec04b213ff81ba8f4c88338767b36a7a4c9f8f3c61d9dbe590be96fb51491`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ENV KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Thu, 01 Jun 2023 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:25 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:25 GMT
USER kong
# Thu, 01 Jun 2023 23:38:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a99a85577e3756d8a7bd71326e7a8674934ddb169bd5a4349103e197a58f983`  
		Last Modified: Thu, 01 Jun 2023 23:39:52 GMT  
		Size: 47.3 MB (47338562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e0e212694b9b9de8b4bcbb4713dbb848f27b1198ac68df26605d26d233870c`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.0`

```console
$ docker pull kong@sha256:9078cc4badc63e1b591ee5e8f1cd97d8a0659b7c783f5fdeeba77e0c6c78e5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.0` - linux; amd64

```console
$ docker pull kong@sha256:cb97b3b9bd4540d09f246f855be72a044b342bbf980c96a0b8117b2700c98ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81311313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5971887ac84cdc4ba0a9c21b9212a6b94d1970e3664b1282ebc11b1954facf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:08 GMT
ARG KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ENV KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Fri, 02 Jun 2023 01:31:42 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:31:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:31:43 GMT
USER kong
# Fri, 02 Jun 2023 01:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:31:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:31:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:31:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:31:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8937d2707ca171dddcc194356d4edef593341b55286e3b54343d1bb304f2c023`  
		Last Modified: Fri, 02 Jun 2023 01:33:24 GMT  
		Size: 50.9 MB (50879757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c105bdc14980907cff3f5de1391848b1ca553a71da5d26d71345454e918caa`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:53f32385a7bb5533c03d3dba190cb1e257b0dfd46a41f6576b0b1fd91245d0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75728888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdec04b213ff81ba8f4c88338767b36a7a4c9f8f3c61d9dbe590be96fb51491`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ENV KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Thu, 01 Jun 2023 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:25 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:25 GMT
USER kong
# Thu, 01 Jun 2023 23:38:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a99a85577e3756d8a7bd71326e7a8674934ddb169bd5a4349103e197a58f983`  
		Last Modified: Thu, 01 Jun 2023 23:39:52 GMT  
		Size: 47.3 MB (47338562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e0e212694b9b9de8b4bcbb4713dbb848f27b1198ac68df26605d26d233870c`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.0-alpine`

```console
$ docker pull kong@sha256:aae539892ee4f08d979274768504d5e592928b1d57a824e3436d627a8588fe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:3.3.0-alpine` - linux; amd64

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

## `kong:3.3.0-ubuntu`

```console
$ docker pull kong@sha256:9078cc4badc63e1b591ee5e8f1cd97d8a0659b7c783f5fdeeba77e0c6c78e5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:cb97b3b9bd4540d09f246f855be72a044b342bbf980c96a0b8117b2700c98ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81311313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5971887ac84cdc4ba0a9c21b9212a6b94d1970e3664b1282ebc11b1954facf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:08 GMT
ARG KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ENV KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Fri, 02 Jun 2023 01:31:42 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:31:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:31:43 GMT
USER kong
# Fri, 02 Jun 2023 01:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:31:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:31:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:31:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:31:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8937d2707ca171dddcc194356d4edef593341b55286e3b54343d1bb304f2c023`  
		Last Modified: Fri, 02 Jun 2023 01:33:24 GMT  
		Size: 50.9 MB (50879757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c105bdc14980907cff3f5de1391848b1ca553a71da5d26d71345454e918caa`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:53f32385a7bb5533c03d3dba190cb1e257b0dfd46a41f6576b0b1fd91245d0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75728888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdec04b213ff81ba8f4c88338767b36a7a4c9f8f3c61d9dbe590be96fb51491`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ENV KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Thu, 01 Jun 2023 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:25 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:25 GMT
USER kong
# Thu, 01 Jun 2023 23:38:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a99a85577e3756d8a7bd71326e7a8674934ddb169bd5a4349103e197a58f983`  
		Last Modified: Thu, 01 Jun 2023 23:39:52 GMT  
		Size: 47.3 MB (47338562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e0e212694b9b9de8b4bcbb4713dbb848f27b1198ac68df26605d26d233870c`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `kong:latest`

```console
$ docker pull kong@sha256:9078cc4badc63e1b591ee5e8f1cd97d8a0659b7c783f5fdeeba77e0c6c78e5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:cb97b3b9bd4540d09f246f855be72a044b342bbf980c96a0b8117b2700c98ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81311313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5971887ac84cdc4ba0a9c21b9212a6b94d1970e3664b1282ebc11b1954facf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:08 GMT
ARG KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ENV KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Fri, 02 Jun 2023 01:31:42 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:31:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:31:43 GMT
USER kong
# Fri, 02 Jun 2023 01:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:31:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:31:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:31:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:31:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8937d2707ca171dddcc194356d4edef593341b55286e3b54343d1bb304f2c023`  
		Last Modified: Fri, 02 Jun 2023 01:33:24 GMT  
		Size: 50.9 MB (50879757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c105bdc14980907cff3f5de1391848b1ca553a71da5d26d71345454e918caa`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:53f32385a7bb5533c03d3dba190cb1e257b0dfd46a41f6576b0b1fd91245d0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75728888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdec04b213ff81ba8f4c88338767b36a7a4c9f8f3c61d9dbe590be96fb51491`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ENV KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Thu, 01 Jun 2023 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:25 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:25 GMT
USER kong
# Thu, 01 Jun 2023 23:38:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a99a85577e3756d8a7bd71326e7a8674934ddb169bd5a4349103e197a58f983`  
		Last Modified: Thu, 01 Jun 2023 23:39:52 GMT  
		Size: 47.3 MB (47338562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e0e212694b9b9de8b4bcbb4713dbb848f27b1198ac68df26605d26d233870c`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:9078cc4badc63e1b591ee5e8f1cd97d8a0659b7c783f5fdeeba77e0c6c78e5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:cb97b3b9bd4540d09f246f855be72a044b342bbf980c96a0b8117b2700c98ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81311313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5971887ac84cdc4ba0a9c21b9212a6b94d1970e3664b1282ebc11b1954facf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:31:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Jun 2023 01:31:08 GMT
ARG ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ENV ASSET=ce
# Fri, 02 Jun 2023 01:31:08 GMT
ARG EE_PORTS
# Fri, 02 Jun 2023 01:31:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Jun 2023 01:31:08 GMT
ARG KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ENV KONG_VERSION=3.3.0
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Fri, 02 Jun 2023 01:31:09 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Fri, 02 Jun 2023 01:31:42 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Jun 2023 01:31:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Jun 2023 01:31:43 GMT
USER kong
# Fri, 02 Jun 2023 01:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:31:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Jun 2023 01:31:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Jun 2023 01:31:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Jun 2023 01:31:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ce35f4f38e7d5b1c78740c274b6a2f5431b8a65c6f90ff823472663ff6b86`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8937d2707ca171dddcc194356d4edef593341b55286e3b54343d1bb304f2c023`  
		Last Modified: Fri, 02 Jun 2023 01:33:24 GMT  
		Size: 50.9 MB (50879757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c105bdc14980907cff3f5de1391848b1ca553a71da5d26d71345454e918caa`  
		Last Modified: Fri, 02 Jun 2023 01:33:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:53f32385a7bb5533c03d3dba190cb1e257b0dfd46a41f6576b0b1fd91245d0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75728888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdec04b213ff81ba8f4c88338767b36a7a4c9f8f3c61d9dbe590be96fb51491`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:38:08 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 01 Jun 2023 23:38:08 GMT
ARG ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ENV ASSET=ce
# Thu, 01 Jun 2023 23:38:08 GMT
ARG EE_PORTS
# Thu, 01 Jun 2023 23:38:08 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ENV KONG_VERSION=3.3.0
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Thu, 01 Jun 2023 23:38:08 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Thu, 01 Jun 2023 23:38:24 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 01 Jun 2023 23:38:25 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 01 Jun 2023 23:38:25 GMT
USER kong
# Thu, 01 Jun 2023 23:38:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:38:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 01 Jun 2023 23:38:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Jun 2023 23:38:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 01 Jun 2023 23:38:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1cbff1aec8aabbdd1de3372b3d35f1c6fc1eef65613f9118d684b4f54d605`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a99a85577e3756d8a7bd71326e7a8674934ddb169bd5a4349103e197a58f983`  
		Last Modified: Thu, 01 Jun 2023 23:39:52 GMT  
		Size: 47.3 MB (47338562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e0e212694b9b9de8b4bcbb4713dbb848f27b1198ac68df26605d26d233870c`  
		Last Modified: Thu, 01 Jun 2023 23:39:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
