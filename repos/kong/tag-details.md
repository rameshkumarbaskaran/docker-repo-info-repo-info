<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.5`](#kong25)
-	[`kong:2.5-ubuntu`](#kong25-ubuntu)
-	[`kong:2.5.1`](#kong251)
-	[`kong:2.5.1-alpine`](#kong251-alpine)
-	[`kong:2.5.1-ubuntu`](#kong251-ubuntu)
-	[`kong:2.6`](#kong26)
-	[`kong:2.6-ubuntu`](#kong26-ubuntu)
-	[`kong:2.6.0`](#kong260)
-	[`kong:2.6.0-alpine`](#kong260-alpine)
-	[`kong:2.6.0-ubuntu`](#kong260-ubuntu)
-	[`kong:2.7`](#kong27)
-	[`kong:2.7-ubuntu`](#kong27-ubuntu)
-	[`kong:2.7.1`](#kong271)
-	[`kong:2.7.1-alpine`](#kong271-alpine)
-	[`kong:2.7.1-ubuntu`](#kong271-ubuntu)
-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.0`](#kong280)
-	[`kong:2.8.0-alpine`](#kong280-alpine)
-	[`kong:2.8.0-ubuntu`](#kong280-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.5`

```console
$ docker pull kong@sha256:d45808b80f0f2a8243b0c513d3c851f1a120923c11ab5f017b58993dcfcaab24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:4b1cbc180eb81167529a6188983fe46b04541fcfbc57559a36ce6b9b0fc1fbbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49823776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeadc3c594a8827c4d3b064f2e53fcb793c2051ff59ec4ea9c479a5ebe4e117`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 10:02:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 19 Mar 2022 10:02:05 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:02:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 19 Mar 2022 10:02:39 GMT
ARG KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:02:39 GMT
ENV KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:02:40 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 19 Mar 2022 10:02:40 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 19 Mar 2022 10:02:40 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 19 Mar 2022 10:02:40 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 19 Mar 2022 10:02:46 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 19 Mar 2022 10:02:47 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:47 GMT
USER kong
# Sat, 19 Mar 2022 10:02:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:47 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:47 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d92b4fe016a2c17fd5ea0165b9c465d159918ada9c2c707177fe2b9e416f94`  
		Last Modified: Sat, 19 Mar 2022 10:04:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707057f111637591d17e47f655d6a53b091e0d94673c7fb97bfb596d97ba9b9f`  
		Last Modified: Sat, 19 Mar 2022 10:05:16 GMT  
		Size: 47.0 MB (47006598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1160abfdffef6aff28b70c420cee11975f37c045127e1a577871e3ff39e1a3`  
		Last Modified: Sat, 19 Mar 2022 10:05:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1c7bf9efb32fa28de661c2ae899d4a6a14f9ce79d386b2352454152a16c38379
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caed0ddb5ef0164709ed61937fff573f4626b54a847241540ef6be8f24bbc07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:52:47 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 21:52:47 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 21:52:48 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 21:52:49 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 21:52:51 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 21:54:40 GMT
ARG KONG_VERSION=2.5.1
# Thu, 17 Mar 2022 21:54:40 GMT
ENV KONG_VERSION=2.5.1
# Thu, 17 Mar 2022 21:54:41 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Thu, 17 Mar 2022 21:54:42 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Thu, 17 Mar 2022 21:54:43 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Thu, 17 Mar 2022 21:54:44 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Thu, 17 Mar 2022 21:55:00 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:55:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:55:01 GMT
USER kong
# Thu, 17 Mar 2022 21:55:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:55:03 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:55:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:55:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:55:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb12b86dd3c64c42cad137cb5166bfedd7adac342c5470de6febc368c397581c`  
		Last Modified: Thu, 17 Mar 2022 21:57:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36224f8957097c0da91bb962f15fb923e49846c8e0b766b147f83d4c6c61a6f7`  
		Last Modified: Thu, 17 Mar 2022 21:58:23 GMT  
		Size: 46.5 MB (46520729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1946ba93a4ee555c8d16a92100725b442df434451d5cc3099d50175e5192afa`  
		Last Modified: Thu, 17 Mar 2022 21:58:15 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:aab0c5f4d3478a5918a08ed69b3a180652929b30e6941e2d6af266eb21510799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:507fb354b6598fd6abc7691726a1bf31e8aa29508ca32b2d8cdaed537d4cc31c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128036244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395e014f670e1e7cb43f9e67007e5d558f824517a99119b26d3ec8b96f5d0488`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 10:01:00 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:01:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 19 Mar 2022 10:02:51 GMT
ARG KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:02:51 GMT
ENV KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:03:11 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 19 Mar 2022 10:03:11 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:03:11 GMT
USER kong
# Sat, 19 Mar 2022 10:03:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:03:12 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:03:12 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:03:12 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:03:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c67433e44b0bd509b36cf0e00dd66e29ccfff7151949737f9bae05975bc49e`  
		Last Modified: Sat, 19 Mar 2022 10:03:43 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592e942e81a6eba97f5d6ab0d456753fe38b29f6783723f7f70d2dcabad388d1`  
		Last Modified: Sat, 19 Mar 2022 10:05:39 GMT  
		Size: 74.4 MB (74387492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e8e97a35b943a2eb8a7c41a3474a39440eaa1fa7028281a291743be87886e8`  
		Last Modified: Sat, 19 Mar 2022 10:05:28 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7fb163125ba0769471c7adccc2609abcd37c3e58afcfb159ab99aa30f5ba58f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125879708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8100ea3c312d55c4a34fcf3706f2584737cc61f1662715a6dd709d77d3f79138`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 31 Aug 2021 01:41:19 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Tue, 31 Aug 2021 01:41:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:41:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:41:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:41:21 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:13:00 GMT
ARG ASSET=ce
# Tue, 31 Aug 2021 03:13:00 GMT
ENV ASSET=ce
# Tue, 31 Aug 2021 03:13:00 GMT
ARG EE_PORTS
# Tue, 31 Aug 2021 03:13:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 31 Aug 2021 03:13:01 GMT
ARG KONG_VERSION=2.5.0
# Tue, 31 Aug 2021 03:13:01 GMT
ENV KONG_VERSION=2.5.0
# Tue, 31 Aug 2021 03:13:24 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 31 Aug 2021 03:13:25 GMT
COPY file:ae813ec19d3fef1de3793f6717c2aed3a9daa94e583e9e55448084541de3c5ff in /docker-entrypoint.sh 
# Tue, 31 Aug 2021 03:13:25 GMT
USER kong
# Tue, 31 Aug 2021 03:13:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Aug 2021 03:13:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 31 Aug 2021 03:13:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 31 Aug 2021 03:13:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 31 Aug 2021 03:13:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85569e0c17003d9cf46a8b94076418863e0abfc5474bb830403acf246947fea7`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32ca509d28808ab7c61361835292ee8eddecd0c0949d658bde0ab1a77ecbf6e`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8168af71f81f1ffa234c301e9cc2ee87b560ad8b74ef4100f8ab4a6abf3a8ad3`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee59a359925630cd377c9610b18f7d7797349cdbabeda7b8c8685852a5ff83`  
		Last Modified: Tue, 31 Aug 2021 03:14:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe71eb414d43ff3fbf75c0de9133ebafceaf672848c6e2c17e4ab47780e97b`  
		Last Modified: Tue, 31 Aug 2021 03:15:00 GMT  
		Size: 59.6 MB (59556314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a45ed64e5c35d56c7aafb050d22218142de8f6d3142eba9294d41638844747`  
		Last Modified: Tue, 31 Aug 2021 03:14:46 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1`

```console
$ docker pull kong@sha256:d45808b80f0f2a8243b0c513d3c851f1a120923c11ab5f017b58993dcfcaab24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1` - linux; amd64

```console
$ docker pull kong@sha256:4b1cbc180eb81167529a6188983fe46b04541fcfbc57559a36ce6b9b0fc1fbbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49823776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeadc3c594a8827c4d3b064f2e53fcb793c2051ff59ec4ea9c479a5ebe4e117`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 10:02:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 19 Mar 2022 10:02:05 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:02:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 19 Mar 2022 10:02:39 GMT
ARG KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:02:39 GMT
ENV KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:02:40 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 19 Mar 2022 10:02:40 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 19 Mar 2022 10:02:40 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 19 Mar 2022 10:02:40 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 19 Mar 2022 10:02:46 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 19 Mar 2022 10:02:47 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:47 GMT
USER kong
# Sat, 19 Mar 2022 10:02:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:47 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:47 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d92b4fe016a2c17fd5ea0165b9c465d159918ada9c2c707177fe2b9e416f94`  
		Last Modified: Sat, 19 Mar 2022 10:04:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707057f111637591d17e47f655d6a53b091e0d94673c7fb97bfb596d97ba9b9f`  
		Last Modified: Sat, 19 Mar 2022 10:05:16 GMT  
		Size: 47.0 MB (47006598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1160abfdffef6aff28b70c420cee11975f37c045127e1a577871e3ff39e1a3`  
		Last Modified: Sat, 19 Mar 2022 10:05:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1c7bf9efb32fa28de661c2ae899d4a6a14f9ce79d386b2352454152a16c38379
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caed0ddb5ef0164709ed61937fff573f4626b54a847241540ef6be8f24bbc07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:52:47 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 21:52:47 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 21:52:48 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 21:52:49 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 21:52:51 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 21:54:40 GMT
ARG KONG_VERSION=2.5.1
# Thu, 17 Mar 2022 21:54:40 GMT
ENV KONG_VERSION=2.5.1
# Thu, 17 Mar 2022 21:54:41 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Thu, 17 Mar 2022 21:54:42 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Thu, 17 Mar 2022 21:54:43 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Thu, 17 Mar 2022 21:54:44 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Thu, 17 Mar 2022 21:55:00 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:55:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:55:01 GMT
USER kong
# Thu, 17 Mar 2022 21:55:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:55:03 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:55:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:55:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:55:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb12b86dd3c64c42cad137cb5166bfedd7adac342c5470de6febc368c397581c`  
		Last Modified: Thu, 17 Mar 2022 21:57:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36224f8957097c0da91bb962f15fb923e49846c8e0b766b147f83d4c6c61a6f7`  
		Last Modified: Thu, 17 Mar 2022 21:58:23 GMT  
		Size: 46.5 MB (46520729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1946ba93a4ee555c8d16a92100725b442df434451d5cc3099d50175e5192afa`  
		Last Modified: Thu, 17 Mar 2022 21:58:15 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1-alpine`

```console
$ docker pull kong@sha256:d45808b80f0f2a8243b0c513d3c851f1a120923c11ab5f017b58993dcfcaab24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:4b1cbc180eb81167529a6188983fe46b04541fcfbc57559a36ce6b9b0fc1fbbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49823776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeadc3c594a8827c4d3b064f2e53fcb793c2051ff59ec4ea9c479a5ebe4e117`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 10:02:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 19 Mar 2022 10:02:05 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:02:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 19 Mar 2022 10:02:39 GMT
ARG KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:02:39 GMT
ENV KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:02:40 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 19 Mar 2022 10:02:40 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 19 Mar 2022 10:02:40 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 19 Mar 2022 10:02:40 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 19 Mar 2022 10:02:46 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 19 Mar 2022 10:02:47 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:47 GMT
USER kong
# Sat, 19 Mar 2022 10:02:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:47 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:47 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d92b4fe016a2c17fd5ea0165b9c465d159918ada9c2c707177fe2b9e416f94`  
		Last Modified: Sat, 19 Mar 2022 10:04:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707057f111637591d17e47f655d6a53b091e0d94673c7fb97bfb596d97ba9b9f`  
		Last Modified: Sat, 19 Mar 2022 10:05:16 GMT  
		Size: 47.0 MB (47006598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1160abfdffef6aff28b70c420cee11975f37c045127e1a577871e3ff39e1a3`  
		Last Modified: Sat, 19 Mar 2022 10:05:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1c7bf9efb32fa28de661c2ae899d4a6a14f9ce79d386b2352454152a16c38379
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caed0ddb5ef0164709ed61937fff573f4626b54a847241540ef6be8f24bbc07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:52:47 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 21:52:47 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 21:52:48 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 21:52:49 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 21:52:51 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 21:54:40 GMT
ARG KONG_VERSION=2.5.1
# Thu, 17 Mar 2022 21:54:40 GMT
ENV KONG_VERSION=2.5.1
# Thu, 17 Mar 2022 21:54:41 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Thu, 17 Mar 2022 21:54:42 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Thu, 17 Mar 2022 21:54:43 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Thu, 17 Mar 2022 21:54:44 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Thu, 17 Mar 2022 21:55:00 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:55:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:55:01 GMT
USER kong
# Thu, 17 Mar 2022 21:55:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:55:03 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:55:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:55:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:55:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb12b86dd3c64c42cad137cb5166bfedd7adac342c5470de6febc368c397581c`  
		Last Modified: Thu, 17 Mar 2022 21:57:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36224f8957097c0da91bb962f15fb923e49846c8e0b766b147f83d4c6c61a6f7`  
		Last Modified: Thu, 17 Mar 2022 21:58:23 GMT  
		Size: 46.5 MB (46520729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1946ba93a4ee555c8d16a92100725b442df434451d5cc3099d50175e5192afa`  
		Last Modified: Thu, 17 Mar 2022 21:58:15 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1-ubuntu`

```console
$ docker pull kong@sha256:ff22308d8b625c2f82a3a64ec84fa556d87e4d607b6095303c503ce9bc1c4994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.5.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:507fb354b6598fd6abc7691726a1bf31e8aa29508ca32b2d8cdaed537d4cc31c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128036244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395e014f670e1e7cb43f9e67007e5d558f824517a99119b26d3ec8b96f5d0488`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 10:01:00 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:01:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 19 Mar 2022 10:02:51 GMT
ARG KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:02:51 GMT
ENV KONG_VERSION=2.5.1
# Sat, 19 Mar 2022 10:03:11 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 19 Mar 2022 10:03:11 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:03:11 GMT
USER kong
# Sat, 19 Mar 2022 10:03:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:03:12 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:03:12 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:03:12 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:03:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c67433e44b0bd509b36cf0e00dd66e29ccfff7151949737f9bae05975bc49e`  
		Last Modified: Sat, 19 Mar 2022 10:03:43 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592e942e81a6eba97f5d6ab0d456753fe38b29f6783723f7f70d2dcabad388d1`  
		Last Modified: Sat, 19 Mar 2022 10:05:39 GMT  
		Size: 74.4 MB (74387492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e8e97a35b943a2eb8a7c41a3474a39440eaa1fa7028281a291743be87886e8`  
		Last Modified: Sat, 19 Mar 2022 10:05:28 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:b9bdd11cc06b03229f0c1e35898d54acd92310d76398633c010d510183164398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

```console
$ docker pull kong@sha256:f413ac0a3eab77656f5c2d0108259a8cc1a5fd0af805375418516738e25a0535
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49848725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1054d88b349d104a2acd156f09225513e53696276318ab3db69fe0a199166a64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 10:02:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 19 Mar 2022 10:02:05 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:02:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 19 Mar 2022 10:02:05 GMT
ARG KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:05 GMT
ENV KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:06 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 19 Mar 2022 10:02:06 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 19 Mar 2022 10:02:06 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 19 Mar 2022 10:02:06 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 19 Mar 2022 10:02:13 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 19 Mar 2022 10:02:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:13 GMT
USER kong
# Sat, 19 Mar 2022 10:02:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d92b4fe016a2c17fd5ea0165b9c465d159918ada9c2c707177fe2b9e416f94`  
		Last Modified: Sat, 19 Mar 2022 10:04:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceaf54b5dac856afe4f47061663b55a88687a6890e7657f202a1726554b609b`  
		Last Modified: Sat, 19 Mar 2022 10:04:35 GMT  
		Size: 47.0 MB (47031545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3121f33e7217f9f51336006401d561046a68c5e62169549ecf0f7e5c7243be`  
		Last Modified: Sat, 19 Mar 2022 10:04:28 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:14d73ade927d58f0038a116d3febd3eca3ed62697b8058579ad005cb50a326c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49275073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6594acf9c884d826ee7ebfe42cccdb19b72f2b55da913538c9d262950e5a20c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:52:47 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 21:52:47 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 21:52:48 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 21:52:49 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 21:52:51 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 21:52:51 GMT
ARG KONG_VERSION=2.6.0
# Thu, 17 Mar 2022 21:52:52 GMT
ENV KONG_VERSION=2.6.0
# Thu, 17 Mar 2022 21:52:53 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Thu, 17 Mar 2022 21:52:54 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Thu, 17 Mar 2022 21:52:55 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Thu, 17 Mar 2022 21:52:56 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Thu, 17 Mar 2022 21:53:11 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:53:12 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:53:12 GMT
USER kong
# Thu, 17 Mar 2022 21:53:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:53:14 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:53:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:53:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:53:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb12b86dd3c64c42cad137cb5166bfedd7adac342c5470de6febc368c397581c`  
		Last Modified: Thu, 17 Mar 2022 21:57:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653571d6f79acf431651c4e3257337ffffae59ab7489eaae62fab2a662c0316a`  
		Last Modified: Thu, 17 Mar 2022 21:58:01 GMT  
		Size: 46.6 MB (46558171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae5a69d67593d4aeb929c27601614ad9717327131165f8c6eedaa11402bc827`  
		Last Modified: Thu, 17 Mar 2022 21:57:52 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:3545c2550639d363f7c1e89539dd3e39861408f0e793fc1a14581a5ac78c3fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:07f7c8f9355aed2cec44bf2711befed17f9b92204c44a7ad7a3d51b4edd6b9b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128081549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a19a8cde9192ee119865d7ead841e03dca30b309747feb8b79acb655bc4ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 10:01:00 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:01:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 19 Mar 2022 10:02:16 GMT
ARG KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:16 GMT
ENV KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:35 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 19 Mar 2022 10:02:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:36 GMT
USER kong
# Sat, 19 Mar 2022 10:02:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:36 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:36 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c67433e44b0bd509b36cf0e00dd66e29ccfff7151949737f9bae05975bc49e`  
		Last Modified: Sat, 19 Mar 2022 10:03:43 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0abcebb975be4e5dd8d465d1d9bd150bd0cd595ab6d637caed958f034b39d1`  
		Last Modified: Sat, 19 Mar 2022 10:04:59 GMT  
		Size: 74.4 MB (74432796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1684028e4bc3f0130ec94a44702a13e0f965a82ad40a13ac86ea0fc49cb4a26e`  
		Last Modified: Sat, 19 Mar 2022 10:04:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0`

```console
$ docker pull kong@sha256:b9bdd11cc06b03229f0c1e35898d54acd92310d76398633c010d510183164398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0` - linux; amd64

```console
$ docker pull kong@sha256:f413ac0a3eab77656f5c2d0108259a8cc1a5fd0af805375418516738e25a0535
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49848725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1054d88b349d104a2acd156f09225513e53696276318ab3db69fe0a199166a64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 10:02:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 19 Mar 2022 10:02:05 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:02:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 19 Mar 2022 10:02:05 GMT
ARG KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:05 GMT
ENV KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:06 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 19 Mar 2022 10:02:06 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 19 Mar 2022 10:02:06 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 19 Mar 2022 10:02:06 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 19 Mar 2022 10:02:13 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 19 Mar 2022 10:02:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:13 GMT
USER kong
# Sat, 19 Mar 2022 10:02:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d92b4fe016a2c17fd5ea0165b9c465d159918ada9c2c707177fe2b9e416f94`  
		Last Modified: Sat, 19 Mar 2022 10:04:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceaf54b5dac856afe4f47061663b55a88687a6890e7657f202a1726554b609b`  
		Last Modified: Sat, 19 Mar 2022 10:04:35 GMT  
		Size: 47.0 MB (47031545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3121f33e7217f9f51336006401d561046a68c5e62169549ecf0f7e5c7243be`  
		Last Modified: Sat, 19 Mar 2022 10:04:28 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:14d73ade927d58f0038a116d3febd3eca3ed62697b8058579ad005cb50a326c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49275073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6594acf9c884d826ee7ebfe42cccdb19b72f2b55da913538c9d262950e5a20c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:52:47 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 21:52:47 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 21:52:48 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 21:52:49 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 21:52:51 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 21:52:51 GMT
ARG KONG_VERSION=2.6.0
# Thu, 17 Mar 2022 21:52:52 GMT
ENV KONG_VERSION=2.6.0
# Thu, 17 Mar 2022 21:52:53 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Thu, 17 Mar 2022 21:52:54 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Thu, 17 Mar 2022 21:52:55 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Thu, 17 Mar 2022 21:52:56 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Thu, 17 Mar 2022 21:53:11 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:53:12 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:53:12 GMT
USER kong
# Thu, 17 Mar 2022 21:53:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:53:14 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:53:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:53:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:53:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb12b86dd3c64c42cad137cb5166bfedd7adac342c5470de6febc368c397581c`  
		Last Modified: Thu, 17 Mar 2022 21:57:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653571d6f79acf431651c4e3257337ffffae59ab7489eaae62fab2a662c0316a`  
		Last Modified: Thu, 17 Mar 2022 21:58:01 GMT  
		Size: 46.6 MB (46558171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae5a69d67593d4aeb929c27601614ad9717327131165f8c6eedaa11402bc827`  
		Last Modified: Thu, 17 Mar 2022 21:57:52 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0-alpine`

```console
$ docker pull kong@sha256:b9bdd11cc06b03229f0c1e35898d54acd92310d76398633c010d510183164398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:f413ac0a3eab77656f5c2d0108259a8cc1a5fd0af805375418516738e25a0535
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49848725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1054d88b349d104a2acd156f09225513e53696276318ab3db69fe0a199166a64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 10:02:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 19 Mar 2022 10:02:05 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:02:05 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:02:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 19 Mar 2022 10:02:05 GMT
ARG KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:05 GMT
ENV KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:06 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 19 Mar 2022 10:02:06 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 19 Mar 2022 10:02:06 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 19 Mar 2022 10:02:06 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 19 Mar 2022 10:02:13 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 19 Mar 2022 10:02:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:13 GMT
USER kong
# Sat, 19 Mar 2022 10:02:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d92b4fe016a2c17fd5ea0165b9c465d159918ada9c2c707177fe2b9e416f94`  
		Last Modified: Sat, 19 Mar 2022 10:04:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceaf54b5dac856afe4f47061663b55a88687a6890e7657f202a1726554b609b`  
		Last Modified: Sat, 19 Mar 2022 10:04:35 GMT  
		Size: 47.0 MB (47031545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3121f33e7217f9f51336006401d561046a68c5e62169549ecf0f7e5c7243be`  
		Last Modified: Sat, 19 Mar 2022 10:04:28 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:14d73ade927d58f0038a116d3febd3eca3ed62697b8058579ad005cb50a326c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49275073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6594acf9c884d826ee7ebfe42cccdb19b72f2b55da913538c9d262950e5a20c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:52:47 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 21:52:47 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 21:52:48 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 21:52:49 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 21:52:51 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 21:52:51 GMT
ARG KONG_VERSION=2.6.0
# Thu, 17 Mar 2022 21:52:52 GMT
ENV KONG_VERSION=2.6.0
# Thu, 17 Mar 2022 21:52:53 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Thu, 17 Mar 2022 21:52:54 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Thu, 17 Mar 2022 21:52:55 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Thu, 17 Mar 2022 21:52:56 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Thu, 17 Mar 2022 21:53:11 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:53:12 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:53:12 GMT
USER kong
# Thu, 17 Mar 2022 21:53:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:53:14 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:53:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:53:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:53:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb12b86dd3c64c42cad137cb5166bfedd7adac342c5470de6febc368c397581c`  
		Last Modified: Thu, 17 Mar 2022 21:57:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653571d6f79acf431651c4e3257337ffffae59ab7489eaae62fab2a662c0316a`  
		Last Modified: Thu, 17 Mar 2022 21:58:01 GMT  
		Size: 46.6 MB (46558171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae5a69d67593d4aeb929c27601614ad9717327131165f8c6eedaa11402bc827`  
		Last Modified: Thu, 17 Mar 2022 21:57:52 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0-ubuntu`

```console
$ docker pull kong@sha256:3545c2550639d363f7c1e89539dd3e39861408f0e793fc1a14581a5ac78c3fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:07f7c8f9355aed2cec44bf2711befed17f9b92204c44a7ad7a3d51b4edd6b9b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128081549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a19a8cde9192ee119865d7ead841e03dca30b309747feb8b79acb655bc4ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 10:01:00 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:01:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 19 Mar 2022 10:02:16 GMT
ARG KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:16 GMT
ENV KONG_VERSION=2.6.0
# Sat, 19 Mar 2022 10:02:35 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 19 Mar 2022 10:02:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:36 GMT
USER kong
# Sat, 19 Mar 2022 10:02:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:36 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:36 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c67433e44b0bd509b36cf0e00dd66e29ccfff7151949737f9bae05975bc49e`  
		Last Modified: Sat, 19 Mar 2022 10:03:43 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0abcebb975be4e5dd8d465d1d9bd150bd0cd595ab6d637caed958f034b39d1`  
		Last Modified: Sat, 19 Mar 2022 10:04:59 GMT  
		Size: 74.4 MB (74432796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1684028e4bc3f0130ec94a44702a13e0f965a82ad40a13ac86ea0fc49cb4a26e`  
		Last Modified: Sat, 19 Mar 2022 10:04:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7`

```console
$ docker pull kong@sha256:4913f0d919d1bab517b23b1b6945cf8774a1c8c106d2f4e87fc7fe152f8bf742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7` - linux; amd64

```console
$ docker pull kong@sha256:7dee2ef04fba5b6d68c844ca64a7fdd245239c5dfe861f77af3ea419a927cc30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50070446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2d43753929e8043a80d4caa3fcd9dcd82b3061fdf89c5afbf7c9ac6c582e36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 12:45:29 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 12:45:29 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 12:45:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 12:45:44 GMT
ARG KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 12:45:44 GMT
ENV KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 12:45:44 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Thu, 17 Mar 2022 12:45:44 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Thu, 17 Mar 2022 12:45:52 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 12:45:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 12:45:52 GMT
USER kong
# Thu, 17 Mar 2022 12:45:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 12:45:53 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 12:45:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 12:45:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 12:45:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e3e05e1ea26f1f6f2bf1773cef7fddadbc475f528069e93e0c6ee25d2a9cd1`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7786f28641ce323aa34c6aa50d244d8960defba113cafd1dc1c88f549618a`  
		Last Modified: Thu, 17 Mar 2022 12:47:06 GMT  
		Size: 47.3 MB (47256798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ade7aade623514700171c9dcd5710fe2eb5aa478ca71092ad881e1cdc4adac`  
		Last Modified: Thu, 17 Mar 2022 12:46:56 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:956a7fc800faeaa7a0af1c1e2772b7ed8fadfa480ebf51ab36d5e7048ec4991d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e129d7a27511d04c6fa0d28ddf8205e00c13da4850c2a44201f20a338d74ab`
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
# Thu, 17 Mar 2022 21:50:30 GMT
ARG KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 21:50:30 GMT
ENV KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 21:50:31 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Thu, 17 Mar 2022 21:50:32 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Thu, 17 Mar 2022 21:50:40 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:50:41 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:50:41 GMT
USER kong
# Thu, 17 Mar 2022 21:50:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:50:43 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:50:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:50:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:50:46 GMT
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
	-	`sha256:7610477de83865e30265342de527ece5469c19798f285b84dd2bcee18dae5b65`  
		Last Modified: Thu, 17 Mar 2022 21:57:38 GMT  
		Size: 46.8 MB (46763013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495db522df3ffd76fdea3ee8e4003ba30efd4b220324f27a5c90d5d99bfbfecf`  
		Last Modified: Thu, 17 Mar 2022 21:57:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7-ubuntu`

```console
$ docker pull kong@sha256:6528e1df1d72a1041267347b9c98b2be6bf17afa9df4a1386e1e4ed81657b9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:4327b09a92132798b1985289c1e9fae2d6b689b37426197548743e581afa0a05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127991905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246a89fc0cb1adebb730e4878ca378db4b509ea471dd903c91c01520176e540d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 10:01:00 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:01:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 19 Mar 2022 10:01:42 GMT
ARG KONG_VERSION=2.7.1
# Sat, 19 Mar 2022 10:01:42 GMT
ENV KONG_VERSION=2.7.1
# Sat, 19 Mar 2022 10:01:42 GMT
ARG KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
# Sat, 19 Mar 2022 10:02:01 GMT
# ARGS: KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 19 Mar 2022 10:02:02 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:02 GMT
USER kong
# Sat, 19 Mar 2022 10:02:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:02 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:02 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c67433e44b0bd509b36cf0e00dd66e29ccfff7151949737f9bae05975bc49e`  
		Last Modified: Sat, 19 Mar 2022 10:03:43 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c0d674696cb4b6831dee0d49d3aaf1770b324760e18ad66199d15dfe67fe11`  
		Last Modified: Sat, 19 Mar 2022 10:04:18 GMT  
		Size: 74.3 MB (74343152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498639a45ea62499f410550f931596227171ebe09fffa32b2f94c4a160f1da38`  
		Last Modified: Sat, 19 Mar 2022 10:04:06 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.1`

```console
$ docker pull kong@sha256:4913f0d919d1bab517b23b1b6945cf8774a1c8c106d2f4e87fc7fe152f8bf742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.1` - linux; amd64

```console
$ docker pull kong@sha256:7dee2ef04fba5b6d68c844ca64a7fdd245239c5dfe861f77af3ea419a927cc30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50070446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2d43753929e8043a80d4caa3fcd9dcd82b3061fdf89c5afbf7c9ac6c582e36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 12:45:29 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 12:45:29 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 12:45:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 12:45:44 GMT
ARG KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 12:45:44 GMT
ENV KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 12:45:44 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Thu, 17 Mar 2022 12:45:44 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Thu, 17 Mar 2022 12:45:52 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 12:45:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 12:45:52 GMT
USER kong
# Thu, 17 Mar 2022 12:45:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 12:45:53 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 12:45:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 12:45:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 12:45:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e3e05e1ea26f1f6f2bf1773cef7fddadbc475f528069e93e0c6ee25d2a9cd1`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7786f28641ce323aa34c6aa50d244d8960defba113cafd1dc1c88f549618a`  
		Last Modified: Thu, 17 Mar 2022 12:47:06 GMT  
		Size: 47.3 MB (47256798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ade7aade623514700171c9dcd5710fe2eb5aa478ca71092ad881e1cdc4adac`  
		Last Modified: Thu, 17 Mar 2022 12:46:56 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:956a7fc800faeaa7a0af1c1e2772b7ed8fadfa480ebf51ab36d5e7048ec4991d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e129d7a27511d04c6fa0d28ddf8205e00c13da4850c2a44201f20a338d74ab`
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
# Thu, 17 Mar 2022 21:50:30 GMT
ARG KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 21:50:30 GMT
ENV KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 21:50:31 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Thu, 17 Mar 2022 21:50:32 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Thu, 17 Mar 2022 21:50:40 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:50:41 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:50:41 GMT
USER kong
# Thu, 17 Mar 2022 21:50:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:50:43 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:50:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:50:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:50:46 GMT
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
	-	`sha256:7610477de83865e30265342de527ece5469c19798f285b84dd2bcee18dae5b65`  
		Last Modified: Thu, 17 Mar 2022 21:57:38 GMT  
		Size: 46.8 MB (46763013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495db522df3ffd76fdea3ee8e4003ba30efd4b220324f27a5c90d5d99bfbfecf`  
		Last Modified: Thu, 17 Mar 2022 21:57:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.1-alpine`

```console
$ docker pull kong@sha256:4913f0d919d1bab517b23b1b6945cf8774a1c8c106d2f4e87fc7fe152f8bf742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:7dee2ef04fba5b6d68c844ca64a7fdd245239c5dfe861f77af3ea419a927cc30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50070446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2d43753929e8043a80d4caa3fcd9dcd82b3061fdf89c5afbf7c9ac6c582e36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 12:45:29 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 12:45:29 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 12:45:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 12:45:44 GMT
ARG KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 12:45:44 GMT
ENV KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 12:45:44 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Thu, 17 Mar 2022 12:45:44 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Thu, 17 Mar 2022 12:45:52 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 12:45:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 12:45:52 GMT
USER kong
# Thu, 17 Mar 2022 12:45:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 12:45:53 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 12:45:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 12:45:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 12:45:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e3e05e1ea26f1f6f2bf1773cef7fddadbc475f528069e93e0c6ee25d2a9cd1`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7786f28641ce323aa34c6aa50d244d8960defba113cafd1dc1c88f549618a`  
		Last Modified: Thu, 17 Mar 2022 12:47:06 GMT  
		Size: 47.3 MB (47256798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ade7aade623514700171c9dcd5710fe2eb5aa478ca71092ad881e1cdc4adac`  
		Last Modified: Thu, 17 Mar 2022 12:46:56 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:956a7fc800faeaa7a0af1c1e2772b7ed8fadfa480ebf51ab36d5e7048ec4991d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e129d7a27511d04c6fa0d28ddf8205e00c13da4850c2a44201f20a338d74ab`
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
# Thu, 17 Mar 2022 21:50:30 GMT
ARG KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 21:50:30 GMT
ENV KONG_VERSION=2.7.1
# Thu, 17 Mar 2022 21:50:31 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Thu, 17 Mar 2022 21:50:32 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Thu, 17 Mar 2022 21:50:40 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 21:50:41 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 21:50:41 GMT
USER kong
# Thu, 17 Mar 2022 21:50:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:50:43 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 21:50:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 21:50:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 21:50:46 GMT
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
	-	`sha256:7610477de83865e30265342de527ece5469c19798f285b84dd2bcee18dae5b65`  
		Last Modified: Thu, 17 Mar 2022 21:57:38 GMT  
		Size: 46.8 MB (46763013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495db522df3ffd76fdea3ee8e4003ba30efd4b220324f27a5c90d5d99bfbfecf`  
		Last Modified: Thu, 17 Mar 2022 21:57:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.1-ubuntu`

```console
$ docker pull kong@sha256:6528e1df1d72a1041267347b9c98b2be6bf17afa9df4a1386e1e4ed81657b9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:4327b09a92132798b1985289c1e9fae2d6b689b37426197548743e581afa0a05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127991905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246a89fc0cb1adebb730e4878ca378db4b509ea471dd903c91c01520176e540d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 10:01:00 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:01:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 19 Mar 2022 10:01:42 GMT
ARG KONG_VERSION=2.7.1
# Sat, 19 Mar 2022 10:01:42 GMT
ENV KONG_VERSION=2.7.1
# Sat, 19 Mar 2022 10:01:42 GMT
ARG KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
# Sat, 19 Mar 2022 10:02:01 GMT
# ARGS: KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 19 Mar 2022 10:02:02 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:02:02 GMT
USER kong
# Sat, 19 Mar 2022 10:02:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:02:02 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:02:02 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:02:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:02:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c67433e44b0bd509b36cf0e00dd66e29ccfff7151949737f9bae05975bc49e`  
		Last Modified: Sat, 19 Mar 2022 10:03:43 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c0d674696cb4b6831dee0d49d3aaf1770b324760e18ad66199d15dfe67fe11`  
		Last Modified: Sat, 19 Mar 2022 10:04:18 GMT  
		Size: 74.3 MB (74343152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498639a45ea62499f410550f931596227171ebe09fffa32b2f94c4a160f1da38`  
		Last Modified: Sat, 19 Mar 2022 10:04:06 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8`

```console
$ docker pull kong@sha256:58990f678d9771ad1d036e2bf737d59fba2194310881b5944b1271a107d7c2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:21236a4e662aea8cff7a62ad2d39f4c845a3ed5f44834bafcb8a7e07001466e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49110785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c413c46038620ade201dd2d46194a758ad537e1c0b805142b43cce00455a9683`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 12:45:29 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 12:45:29 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 12:45:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ENV KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Thu, 17 Mar 2022 12:45:37 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 12:45:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 12:45:38 GMT
USER kong
# Thu, 17 Mar 2022 12:45:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 12:45:38 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 12:45:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 12:45:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 12:45:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e3e05e1ea26f1f6f2bf1773cef7fddadbc475f528069e93e0c6ee25d2a9cd1`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d9b64b8a8870acc6d3d02360b77e5b0b21b1f03289a06bb4de681087df862e`  
		Last Modified: Thu, 17 Mar 2022 12:46:39 GMT  
		Size: 46.3 MB (46297137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf0f9d59c872d6017fdf14b8490fadf5a6e94d83cef15b4f70d56748318c2c`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

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

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:c8122ca089105511c2085ed8aea1e8fd1788455b34144cc680f7838963cc615d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3731d007b878f8e3fdce1178a81155a70da39e9df52db4a649dc3380bfcdcfa1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121212173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651d05fa278423d65bbb94ffc94399f100d3ce9b0080af63ef6157288499ccb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 10:01:00 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:01:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 19 Mar 2022 10:01:00 GMT
ARG KONG_VERSION=2.8.0
# Sat, 19 Mar 2022 10:01:00 GMT
ENV KONG_VERSION=2.8.0
# Sat, 19 Mar 2022 10:01:01 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Sat, 19 Mar 2022 10:01:30 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 19 Mar 2022 10:01:31 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:01:31 GMT
USER kong
# Sat, 19 Mar 2022 10:01:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:01:31 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:01:31 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:01:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:01:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c67433e44b0bd509b36cf0e00dd66e29ccfff7151949737f9bae05975bc49e`  
		Last Modified: Sat, 19 Mar 2022 10:03:43 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d2db58368c37d4ddf4a70e8f2b4a882135dd54f2c87d59ed21eed1eb5fb9a6`  
		Last Modified: Sat, 19 Mar 2022 10:03:53 GMT  
		Size: 67.6 MB (67563420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4038a088535540842005ce5cbf0b3a312814d8e7c28fa8e4ee24f0734446844`  
		Last Modified: Sat, 19 Mar 2022 10:03:41 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.0`

```console
$ docker pull kong@sha256:58990f678d9771ad1d036e2bf737d59fba2194310881b5944b1271a107d7c2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.0` - linux; amd64

```console
$ docker pull kong@sha256:21236a4e662aea8cff7a62ad2d39f4c845a3ed5f44834bafcb8a7e07001466e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49110785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c413c46038620ade201dd2d46194a758ad537e1c0b805142b43cce00455a9683`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 12:45:29 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 12:45:29 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 12:45:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ENV KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Thu, 17 Mar 2022 12:45:37 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 12:45:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 12:45:38 GMT
USER kong
# Thu, 17 Mar 2022 12:45:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 12:45:38 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 12:45:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 12:45:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 12:45:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e3e05e1ea26f1f6f2bf1773cef7fddadbc475f528069e93e0c6ee25d2a9cd1`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d9b64b8a8870acc6d3d02360b77e5b0b21b1f03289a06bb4de681087df862e`  
		Last Modified: Thu, 17 Mar 2022 12:46:39 GMT  
		Size: 46.3 MB (46297137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf0f9d59c872d6017fdf14b8490fadf5a6e94d83cef15b4f70d56748318c2c`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.0` - linux; arm64 variant v8

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

## `kong:2.8.0-alpine`

```console
$ docker pull kong@sha256:58990f678d9771ad1d036e2bf737d59fba2194310881b5944b1271a107d7c2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:21236a4e662aea8cff7a62ad2d39f4c845a3ed5f44834bafcb8a7e07001466e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49110785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c413c46038620ade201dd2d46194a758ad537e1c0b805142b43cce00455a9683`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 12:45:29 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 12:45:29 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 12:45:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ENV KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Thu, 17 Mar 2022 12:45:37 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 12:45:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 12:45:38 GMT
USER kong
# Thu, 17 Mar 2022 12:45:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 12:45:38 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 12:45:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 12:45:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 12:45:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e3e05e1ea26f1f6f2bf1773cef7fddadbc475f528069e93e0c6ee25d2a9cd1`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d9b64b8a8870acc6d3d02360b77e5b0b21b1f03289a06bb4de681087df862e`  
		Last Modified: Thu, 17 Mar 2022 12:46:39 GMT  
		Size: 46.3 MB (46297137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf0f9d59c872d6017fdf14b8490fadf5a6e94d83cef15b4f70d56748318c2c`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.0-alpine` - linux; arm64 variant v8

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

## `kong:2.8.0-ubuntu`

```console
$ docker pull kong@sha256:c8122ca089105511c2085ed8aea1e8fd1788455b34144cc680f7838963cc615d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3731d007b878f8e3fdce1178a81155a70da39e9df52db4a649dc3380bfcdcfa1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121212173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651d05fa278423d65bbb94ffc94399f100d3ce9b0080af63ef6157288499ccb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 10:01:00 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:01:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 19 Mar 2022 10:01:00 GMT
ARG KONG_VERSION=2.8.0
# Sat, 19 Mar 2022 10:01:00 GMT
ENV KONG_VERSION=2.8.0
# Sat, 19 Mar 2022 10:01:01 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Sat, 19 Mar 2022 10:01:30 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 19 Mar 2022 10:01:31 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:01:31 GMT
USER kong
# Sat, 19 Mar 2022 10:01:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:01:31 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:01:31 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:01:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:01:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c67433e44b0bd509b36cf0e00dd66e29ccfff7151949737f9bae05975bc49e`  
		Last Modified: Sat, 19 Mar 2022 10:03:43 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d2db58368c37d4ddf4a70e8f2b4a882135dd54f2c87d59ed21eed1eb5fb9a6`  
		Last Modified: Sat, 19 Mar 2022 10:03:53 GMT  
		Size: 67.6 MB (67563420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4038a088535540842005ce5cbf0b3a312814d8e7c28fa8e4ee24f0734446844`  
		Last Modified: Sat, 19 Mar 2022 10:03:41 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:58990f678d9771ad1d036e2bf737d59fba2194310881b5944b1271a107d7c2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:21236a4e662aea8cff7a62ad2d39f4c845a3ed5f44834bafcb8a7e07001466e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49110785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c413c46038620ade201dd2d46194a758ad537e1c0b805142b43cce00455a9683`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 12:45:29 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 12:45:29 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 12:45:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ENV KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Thu, 17 Mar 2022 12:45:37 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 12:45:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 12:45:38 GMT
USER kong
# Thu, 17 Mar 2022 12:45:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 12:45:38 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 12:45:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 12:45:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 12:45:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e3e05e1ea26f1f6f2bf1773cef7fddadbc475f528069e93e0c6ee25d2a9cd1`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d9b64b8a8870acc6d3d02360b77e5b0b21b1f03289a06bb4de681087df862e`  
		Last Modified: Thu, 17 Mar 2022 12:46:39 GMT  
		Size: 46.3 MB (46297137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf0f9d59c872d6017fdf14b8490fadf5a6e94d83cef15b4f70d56748318c2c`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

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

## `kong:latest`

```console
$ docker pull kong@sha256:58990f678d9771ad1d036e2bf737d59fba2194310881b5944b1271a107d7c2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:21236a4e662aea8cff7a62ad2d39f4c845a3ed5f44834bafcb8a7e07001466e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49110785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c413c46038620ade201dd2d46194a758ad537e1c0b805142b43cce00455a9683`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 12:45:29 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Mar 2022 12:45:29 GMT
ARG ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ENV ASSET=ce
# Thu, 17 Mar 2022 12:45:30 GMT
ARG EE_PORTS
# Thu, 17 Mar 2022 12:45:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ENV KONG_VERSION=2.8.0
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Thu, 17 Mar 2022 12:45:30 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Thu, 17 Mar 2022 12:45:37 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Thu, 17 Mar 2022 12:45:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 17 Mar 2022 12:45:38 GMT
USER kong
# Thu, 17 Mar 2022 12:45:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 12:45:38 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Mar 2022 12:45:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 12:45:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 17 Mar 2022 12:45:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e3e05e1ea26f1f6f2bf1773cef7fddadbc475f528069e93e0c6ee25d2a9cd1`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d9b64b8a8870acc6d3d02360b77e5b0b21b1f03289a06bb4de681087df862e`  
		Last Modified: Thu, 17 Mar 2022 12:46:39 GMT  
		Size: 46.3 MB (46297137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf0f9d59c872d6017fdf14b8490fadf5a6e94d83cef15b4f70d56748318c2c`  
		Last Modified: Thu, 17 Mar 2022 12:46:30 GMT  
		Size: 882.0 B  
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

## `kong:ubuntu`

```console
$ docker pull kong@sha256:4402a18ea19646351543a44f5437f7a3c0c2e8665697ac1d270ce35fc12754a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3731d007b878f8e3fdce1178a81155a70da39e9df52db4a649dc3380bfcdcfa1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121212173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651d05fa278423d65bbb94ffc94399f100d3ce9b0080af63ef6157288499ccb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 10:01:00 GMT
ARG ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ENV ASSET=ce
# Sat, 19 Mar 2022 10:01:00 GMT
ARG EE_PORTS
# Sat, 19 Mar 2022 10:01:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 19 Mar 2022 10:01:00 GMT
ARG KONG_VERSION=2.8.0
# Sat, 19 Mar 2022 10:01:00 GMT
ENV KONG_VERSION=2.8.0
# Sat, 19 Mar 2022 10:01:01 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Sat, 19 Mar 2022 10:01:30 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 19 Mar 2022 10:01:31 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 19 Mar 2022 10:01:31 GMT
USER kong
# Sat, 19 Mar 2022 10:01:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 10:01:31 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 19 Mar 2022 10:01:31 GMT
STOPSIGNAL SIGQUIT
# Sat, 19 Mar 2022 10:01:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 19 Mar 2022 10:01:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c67433e44b0bd509b36cf0e00dd66e29ccfff7151949737f9bae05975bc49e`  
		Last Modified: Sat, 19 Mar 2022 10:03:43 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d2db58368c37d4ddf4a70e8f2b4a882135dd54f2c87d59ed21eed1eb5fb9a6`  
		Last Modified: Sat, 19 Mar 2022 10:03:53 GMT  
		Size: 67.6 MB (67563420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4038a088535540842005ce5cbf0b3a312814d8e7c28fa8e4ee24f0734446844`  
		Last Modified: Sat, 19 Mar 2022 10:03:41 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7fb163125ba0769471c7adccc2609abcd37c3e58afcfb159ab99aa30f5ba58f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125879708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8100ea3c312d55c4a34fcf3706f2584737cc61f1662715a6dd709d77d3f79138`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 31 Aug 2021 01:41:19 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Tue, 31 Aug 2021 01:41:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:41:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:41:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:41:21 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:13:00 GMT
ARG ASSET=ce
# Tue, 31 Aug 2021 03:13:00 GMT
ENV ASSET=ce
# Tue, 31 Aug 2021 03:13:00 GMT
ARG EE_PORTS
# Tue, 31 Aug 2021 03:13:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 31 Aug 2021 03:13:01 GMT
ARG KONG_VERSION=2.5.0
# Tue, 31 Aug 2021 03:13:01 GMT
ENV KONG_VERSION=2.5.0
# Tue, 31 Aug 2021 03:13:24 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 31 Aug 2021 03:13:25 GMT
COPY file:ae813ec19d3fef1de3793f6717c2aed3a9daa94e583e9e55448084541de3c5ff in /docker-entrypoint.sh 
# Tue, 31 Aug 2021 03:13:25 GMT
USER kong
# Tue, 31 Aug 2021 03:13:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Aug 2021 03:13:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 31 Aug 2021 03:13:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 31 Aug 2021 03:13:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 31 Aug 2021 03:13:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85569e0c17003d9cf46a8b94076418863e0abfc5474bb830403acf246947fea7`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32ca509d28808ab7c61361835292ee8eddecd0c0949d658bde0ab1a77ecbf6e`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8168af71f81f1ffa234c301e9cc2ee87b560ad8b74ef4100f8ab4a6abf3a8ad3`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee59a359925630cd377c9610b18f7d7797349cdbabeda7b8c8685852a5ff83`  
		Last Modified: Tue, 31 Aug 2021 03:14:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe71eb414d43ff3fbf75c0de9133ebafceaf672848c6e2c17e4ab47780e97b`  
		Last Modified: Tue, 31 Aug 2021 03:15:00 GMT  
		Size: 59.6 MB (59556314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a45ed64e5c35d56c7aafb050d22218142de8f6d3142eba9294d41638844747`  
		Last Modified: Tue, 31 Aug 2021 03:14:46 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
