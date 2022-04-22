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
-	[`kong:2.6.1`](#kong261)
-	[`kong:2.6.1-alpine`](#kong261-alpine)
-	[`kong:2.6.1-ubuntu`](#kong261-ubuntu)
-	[`kong:2.7`](#kong27)
-	[`kong:2.7-ubuntu`](#kong27-ubuntu)
-	[`kong:2.7.1`](#kong271)
-	[`kong:2.7.1-alpine`](#kong271-alpine)
-	[`kong:2.7.1-ubuntu`](#kong271-ubuntu)
-	[`kong:2.7.2`](#kong272)
-	[`kong:2.7.2-alpine`](#kong272-alpine)
-	[`kong:2.7.2-ubuntu`](#kong272-ubuntu)
-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.0`](#kong280)
-	[`kong:2.8.0-alpine`](#kong280-alpine)
-	[`kong:2.8.0-ubuntu`](#kong280-ubuntu)
-	[`kong:2.8.1`](#kong281)
-	[`kong:2.8.1-alpine`](#kong281-alpine)
-	[`kong:2.8.1-ubuntu`](#kong281-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.5`

```console
$ docker pull kong@sha256:41e3edb43d99e58372ad516d02d7723dd4addfbb058cb0bc6f6f7ad224d4f383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:154142e5fd657d9db0e53d9c2f2bb9d3f8690754117153217c7e2c26daec1633
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4df8ab4c6b478a834567e91b0c4afaa8f612d2dd2ad82ef1638dffa8a1791`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:52 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:53 GMT
USER kong
# Tue, 05 Apr 2022 07:18:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e19ff8ee1a3d712fb5a9b15e5dc3975135eabb0db2bdc9d86987b1dc0ab312`  
		Last Modified: Tue, 05 Apr 2022 07:20:38 GMT  
		Size: 47.0 MB (47006838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca93a317bbe9559f2a86be6eb2d745765ebaf28fb2f60aa5c32f0fb28634f5`  
		Last Modified: Tue, 05 Apr 2022 07:20:30 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40bc1b80631be6572ebdd0b3297cf1b405d96eb55605a2843f7395d4c07bd914
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ef302d4e9c486b95849bf1d9380438c9704379c74b16ab5a1a2d9f26b4df54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:28:09 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:10 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:11 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:12 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:13 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:14 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:23 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:28:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:28:24 GMT
USER kong
# Tue, 05 Apr 2022 14:28:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:28:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:28:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:28:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:28:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099f94dcde963cbb40fd4c0b539ebda765c2a4ee6973d14bb0528df4fa3835`  
		Last Modified: Tue, 05 Apr 2022 14:32:09 GMT  
		Size: 46.5 MB (46519329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406022bc9bda03a0ac64449c49805df757f7800fc95c620c9ecc541d65b30820`  
		Last Modified: Tue, 05 Apr 2022 14:32:01 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:509b7b01d9a41a1ae3f59e6e43c86c6105db86bcef4bb69ca81fa26d22bad7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e080982bb2dd65711c2536a7f717b8362c6e4475686b832f2f165b25a3c4333b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128040663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fa984aaaf53b42d4b09e2ed225b31b42b42fdf0376b2e0f14212daf7e84a37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 04:02:39 GMT
ARG KONG_VERSION=2.5.1
# Fri, 22 Apr 2022 04:02:39 GMT
ENV KONG_VERSION=2.5.1
# Fri, 22 Apr 2022 04:02:58 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:02:59 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:02:59 GMT
USER kong
# Fri, 22 Apr 2022 04:02:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:02:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:02:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:03:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:03:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2790a79a6a403aec46803f3882103a9b1662fd11f6688c8b20174d314544bf2`  
		Last Modified: Fri, 22 Apr 2022 04:05:59 GMT  
		Size: 74.4 MB (74391820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b023be5ceaced23f193a17d528d24dfc392a75140144e21ea2cca48d121b9`  
		Last Modified: Fri, 22 Apr 2022 04:05:47 GMT  
		Size: 883.0 B  
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
$ docker pull kong@sha256:41e3edb43d99e58372ad516d02d7723dd4addfbb058cb0bc6f6f7ad224d4f383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1` - linux; amd64

```console
$ docker pull kong@sha256:154142e5fd657d9db0e53d9c2f2bb9d3f8690754117153217c7e2c26daec1633
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4df8ab4c6b478a834567e91b0c4afaa8f612d2dd2ad82ef1638dffa8a1791`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:52 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:53 GMT
USER kong
# Tue, 05 Apr 2022 07:18:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e19ff8ee1a3d712fb5a9b15e5dc3975135eabb0db2bdc9d86987b1dc0ab312`  
		Last Modified: Tue, 05 Apr 2022 07:20:38 GMT  
		Size: 47.0 MB (47006838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca93a317bbe9559f2a86be6eb2d745765ebaf28fb2f60aa5c32f0fb28634f5`  
		Last Modified: Tue, 05 Apr 2022 07:20:30 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40bc1b80631be6572ebdd0b3297cf1b405d96eb55605a2843f7395d4c07bd914
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ef302d4e9c486b95849bf1d9380438c9704379c74b16ab5a1a2d9f26b4df54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:28:09 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:10 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:11 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:12 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:13 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:14 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:23 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:28:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:28:24 GMT
USER kong
# Tue, 05 Apr 2022 14:28:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:28:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:28:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:28:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:28:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099f94dcde963cbb40fd4c0b539ebda765c2a4ee6973d14bb0528df4fa3835`  
		Last Modified: Tue, 05 Apr 2022 14:32:09 GMT  
		Size: 46.5 MB (46519329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406022bc9bda03a0ac64449c49805df757f7800fc95c620c9ecc541d65b30820`  
		Last Modified: Tue, 05 Apr 2022 14:32:01 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1-alpine`

```console
$ docker pull kong@sha256:41e3edb43d99e58372ad516d02d7723dd4addfbb058cb0bc6f6f7ad224d4f383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:154142e5fd657d9db0e53d9c2f2bb9d3f8690754117153217c7e2c26daec1633
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4df8ab4c6b478a834567e91b0c4afaa8f612d2dd2ad82ef1638dffa8a1791`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:52 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:53 GMT
USER kong
# Tue, 05 Apr 2022 07:18:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e19ff8ee1a3d712fb5a9b15e5dc3975135eabb0db2bdc9d86987b1dc0ab312`  
		Last Modified: Tue, 05 Apr 2022 07:20:38 GMT  
		Size: 47.0 MB (47006838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca93a317bbe9559f2a86be6eb2d745765ebaf28fb2f60aa5c32f0fb28634f5`  
		Last Modified: Tue, 05 Apr 2022 07:20:30 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40bc1b80631be6572ebdd0b3297cf1b405d96eb55605a2843f7395d4c07bd914
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ef302d4e9c486b95849bf1d9380438c9704379c74b16ab5a1a2d9f26b4df54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:28:09 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:10 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:11 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:12 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:13 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:14 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:23 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:28:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:28:24 GMT
USER kong
# Tue, 05 Apr 2022 14:28:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:28:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:28:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:28:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:28:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099f94dcde963cbb40fd4c0b539ebda765c2a4ee6973d14bb0528df4fa3835`  
		Last Modified: Tue, 05 Apr 2022 14:32:09 GMT  
		Size: 46.5 MB (46519329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406022bc9bda03a0ac64449c49805df757f7800fc95c620c9ecc541d65b30820`  
		Last Modified: Tue, 05 Apr 2022 14:32:01 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1-ubuntu`

```console
$ docker pull kong@sha256:56e22c392875e145993a3de61709d4cd0a82c70c07e99b0960249039f7b96697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.5.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e080982bb2dd65711c2536a7f717b8362c6e4475686b832f2f165b25a3c4333b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128040663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fa984aaaf53b42d4b09e2ed225b31b42b42fdf0376b2e0f14212daf7e84a37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 04:02:39 GMT
ARG KONG_VERSION=2.5.1
# Fri, 22 Apr 2022 04:02:39 GMT
ENV KONG_VERSION=2.5.1
# Fri, 22 Apr 2022 04:02:58 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:02:59 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:02:59 GMT
USER kong
# Fri, 22 Apr 2022 04:02:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:02:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:02:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:03:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:03:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2790a79a6a403aec46803f3882103a9b1662fd11f6688c8b20174d314544bf2`  
		Last Modified: Fri, 22 Apr 2022 04:05:59 GMT  
		Size: 74.4 MB (74391820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b023be5ceaced23f193a17d528d24dfc392a75140144e21ea2cca48d121b9`  
		Last Modified: Fri, 22 Apr 2022 04:05:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:e44b180d4cca4d068923ae7e0b12c657ea308fca884098db1f802a4321e2c6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

```console
$ docker pull kong@sha256:a68fadbfb98fa3af88866ae49f51c42509a4ab329cfc48fb461d93764901c3ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d25cced91d05f9b228b3df44b49d24d490baeafeac92210ae3c83525d14c9b`
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
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 19:32:51 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:52 GMT
USER kong
# Tue, 12 Apr 2022 19:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:52 GMT
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
	-	`sha256:e846119c04e88b6dc84b3411cf74dde70115ceaa39a9dc3801638e336f40ff6c`  
		Last Modified: Tue, 12 Apr 2022 19:35:40 GMT  
		Size: 47.4 MB (47393221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d957996ac9c41a86d979da49d6d918aa912d47a5e8c14e6b3abef267167b47`  
		Last Modified: Tue, 12 Apr 2022 19:35:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:985bd739862dfba2323e1ef2edfe4b6510aff21ed446d78fd55abf634355a764
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42260facc31b5de9fd189f8a7b54fc41e97032df13c475e688c1cfb6bad4b2`
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
# Tue, 12 Apr 2022 20:05:22 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:23 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:24 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 20:05:25 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 20:05:42 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:05:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:05:43 GMT
USER kong
# Tue, 12 Apr 2022 20:05:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:05:45 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:05:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:05:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:05:48 GMT
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
	-	`sha256:486691177c648ec000964290cee697eab648dbfe2f56efc837a618da681bee22`  
		Last Modified: Tue, 12 Apr 2022 20:11:59 GMT  
		Size: 46.9 MB (46902616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826214118a31a9c5bc16f53e85a4afe7e72467d247ce5ef4a15ebb2c4b11f330`  
		Last Modified: Tue, 12 Apr 2022 20:11:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:11e0474d3c3cc2078f69cd5022d9bcd3f9965d549b7463206a8697f273c85134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e2e70185c29900aca7455bae364b1235dce6f1f657b18bde9580b048546aef8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128172212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c205c6d6e79905c8a5f839b9e60ed2f405d51f58ed64e567abce7e2c3c2c2e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 04:01:44 GMT
ARG KONG_VERSION=2.6.1
# Fri, 22 Apr 2022 04:01:44 GMT
ENV KONG_VERSION=2.6.1
# Fri, 22 Apr 2022 04:01:44 GMT
ARG KONG_SHA256=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Fri, 22 Apr 2022 04:02:04 GMT
# ARGS: KONG_SHA256=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:02:05 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:02:05 GMT
USER kong
# Fri, 22 Apr 2022 04:02:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:02:05 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:02:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:02:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:02:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f143a86548988add2722c52d2f96f24eeef7e805e5e3ef08d1a1f798ed22fb`  
		Last Modified: Fri, 22 Apr 2022 04:05:16 GMT  
		Size: 74.5 MB (74523371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363b17a0055540de2963a7b38cc39c1d41229d331039536dfe8d0bfd16490175`  
		Last Modified: Fri, 22 Apr 2022 04:05:04 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0`

```console
$ docker pull kong@sha256:28f74e81f2d5eef6df34aaf806c177900be52bc2ac9e204c9545203d60ecf8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0` - linux; amd64

```console
$ docker pull kong@sha256:c3d6a0453bca195a12b1e82a74afacecf5506a449492a3786b925cfb9ca4f3bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49851980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5640b9319c0ada43764602002fbe5122da3b9f35ac719498de95b87c39a6f7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:40 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:40 GMT
USER kong
# Tue, 05 Apr 2022 07:18:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:40 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77326087f7969514a492f9b51c9551af57cce74868e026bb20771e97b909ee61`  
		Last Modified: Tue, 05 Apr 2022 07:20:17 GMT  
		Size: 47.0 MB (47032599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e3fa1a6a1f75401c16c56dd497322a8801080e7e047952a17ee44d660848d`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf6164f986d92b75438706bf956f45eebb79f96532836b7a288ee069053f15db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49275254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b2de22d4ad9f1c985b93d3f0ca687a0bea88c9a09fc9d2137ff18dd557ecf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:26:09 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:10 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:11 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:12 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:13 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:14 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:33 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:26:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:26:34 GMT
USER kong
# Tue, 05 Apr 2022 14:26:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:26:36 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:26:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:26:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:26:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bf8e846a5b2efcef66530cbc0ac4c23db06f8e5c297227076ac2a714d14157`  
		Last Modified: Tue, 05 Apr 2022 14:31:47 GMT  
		Size: 46.6 MB (46556851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcf1b755d2953c1384dce92ef08cac677413d9b516f2f4a352825733c77b7bc`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0-alpine`

```console
$ docker pull kong@sha256:28f74e81f2d5eef6df34aaf806c177900be52bc2ac9e204c9545203d60ecf8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:c3d6a0453bca195a12b1e82a74afacecf5506a449492a3786b925cfb9ca4f3bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49851980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5640b9319c0ada43764602002fbe5122da3b9f35ac719498de95b87c39a6f7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:40 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:40 GMT
USER kong
# Tue, 05 Apr 2022 07:18:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:40 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77326087f7969514a492f9b51c9551af57cce74868e026bb20771e97b909ee61`  
		Last Modified: Tue, 05 Apr 2022 07:20:17 GMT  
		Size: 47.0 MB (47032599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e3fa1a6a1f75401c16c56dd497322a8801080e7e047952a17ee44d660848d`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf6164f986d92b75438706bf956f45eebb79f96532836b7a288ee069053f15db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49275254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b2de22d4ad9f1c985b93d3f0ca687a0bea88c9a09fc9d2137ff18dd557ecf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:26:09 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:10 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:11 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:12 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:13 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:14 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:33 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:26:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:26:34 GMT
USER kong
# Tue, 05 Apr 2022 14:26:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:26:36 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:26:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:26:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:26:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bf8e846a5b2efcef66530cbc0ac4c23db06f8e5c297227076ac2a714d14157`  
		Last Modified: Tue, 05 Apr 2022 14:31:47 GMT  
		Size: 46.6 MB (46556851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcf1b755d2953c1384dce92ef08cac677413d9b516f2f4a352825733c77b7bc`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0-ubuntu`

```console
$ docker pull kong@sha256:5efb1273dbe40ec34ca63699dbfb0bd6173a6bf838db2302fb96966c7c389610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8039f612580a3b6a394add8f61503f8cad31bb1197da2fc320d2872442ab5823
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128081691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1899d80e0193c5043e50d7beb3765f0dfa0629b999f2e9c55113d7c5ca5e976e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 04:02:14 GMT
ARG KONG_VERSION=2.6.0
# Fri, 22 Apr 2022 04:02:14 GMT
ENV KONG_VERSION=2.6.0
# Fri, 22 Apr 2022 04:02:33 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:02:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:02:34 GMT
USER kong
# Fri, 22 Apr 2022 04:02:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:02:34 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:02:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:02:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:02:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4921cdee47c420c74fa4445dcfd28f0df66a1d54e980273ac82af5a97cb8c289`  
		Last Modified: Fri, 22 Apr 2022 04:05:39 GMT  
		Size: 74.4 MB (74432851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c74d5e955ddd44ddbc834edc7fe71fd5ac5e44a8bae72bbad021fcf97017b6`  
		Last Modified: Fri, 22 Apr 2022 04:05:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1`

```console
$ docker pull kong@sha256:e44b180d4cca4d068923ae7e0b12c657ea308fca884098db1f802a4321e2c6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1` - linux; amd64

```console
$ docker pull kong@sha256:a68fadbfb98fa3af88866ae49f51c42509a4ab329cfc48fb461d93764901c3ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d25cced91d05f9b228b3df44b49d24d490baeafeac92210ae3c83525d14c9b`
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
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 19:32:51 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:52 GMT
USER kong
# Tue, 12 Apr 2022 19:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:52 GMT
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
	-	`sha256:e846119c04e88b6dc84b3411cf74dde70115ceaa39a9dc3801638e336f40ff6c`  
		Last Modified: Tue, 12 Apr 2022 19:35:40 GMT  
		Size: 47.4 MB (47393221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d957996ac9c41a86d979da49d6d918aa912d47a5e8c14e6b3abef267167b47`  
		Last Modified: Tue, 12 Apr 2022 19:35:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:985bd739862dfba2323e1ef2edfe4b6510aff21ed446d78fd55abf634355a764
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42260facc31b5de9fd189f8a7b54fc41e97032df13c475e688c1cfb6bad4b2`
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
# Tue, 12 Apr 2022 20:05:22 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:23 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:24 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 20:05:25 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 20:05:42 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:05:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:05:43 GMT
USER kong
# Tue, 12 Apr 2022 20:05:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:05:45 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:05:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:05:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:05:48 GMT
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
	-	`sha256:486691177c648ec000964290cee697eab648dbfe2f56efc837a618da681bee22`  
		Last Modified: Tue, 12 Apr 2022 20:11:59 GMT  
		Size: 46.9 MB (46902616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826214118a31a9c5bc16f53e85a4afe7e72467d247ce5ef4a15ebb2c4b11f330`  
		Last Modified: Tue, 12 Apr 2022 20:11:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-alpine`

```console
$ docker pull kong@sha256:e44b180d4cca4d068923ae7e0b12c657ea308fca884098db1f802a4321e2c6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:a68fadbfb98fa3af88866ae49f51c42509a4ab329cfc48fb461d93764901c3ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d25cced91d05f9b228b3df44b49d24d490baeafeac92210ae3c83525d14c9b`
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
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 19:32:51 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:52 GMT
USER kong
# Tue, 12 Apr 2022 19:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:52 GMT
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
	-	`sha256:e846119c04e88b6dc84b3411cf74dde70115ceaa39a9dc3801638e336f40ff6c`  
		Last Modified: Tue, 12 Apr 2022 19:35:40 GMT  
		Size: 47.4 MB (47393221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d957996ac9c41a86d979da49d6d918aa912d47a5e8c14e6b3abef267167b47`  
		Last Modified: Tue, 12 Apr 2022 19:35:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:985bd739862dfba2323e1ef2edfe4b6510aff21ed446d78fd55abf634355a764
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42260facc31b5de9fd189f8a7b54fc41e97032df13c475e688c1cfb6bad4b2`
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
# Tue, 12 Apr 2022 20:05:22 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:23 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:24 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 20:05:25 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 20:05:42 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:05:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:05:43 GMT
USER kong
# Tue, 12 Apr 2022 20:05:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:05:45 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:05:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:05:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:05:48 GMT
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
	-	`sha256:486691177c648ec000964290cee697eab648dbfe2f56efc837a618da681bee22`  
		Last Modified: Tue, 12 Apr 2022 20:11:59 GMT  
		Size: 46.9 MB (46902616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826214118a31a9c5bc16f53e85a4afe7e72467d247ce5ef4a15ebb2c4b11f330`  
		Last Modified: Tue, 12 Apr 2022 20:11:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-ubuntu`

```console
$ docker pull kong@sha256:11e0474d3c3cc2078f69cd5022d9bcd3f9965d549b7463206a8697f273c85134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e2e70185c29900aca7455bae364b1235dce6f1f657b18bde9580b048546aef8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128172212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c205c6d6e79905c8a5f839b9e60ed2f405d51f58ed64e567abce7e2c3c2c2e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 04:01:44 GMT
ARG KONG_VERSION=2.6.1
# Fri, 22 Apr 2022 04:01:44 GMT
ENV KONG_VERSION=2.6.1
# Fri, 22 Apr 2022 04:01:44 GMT
ARG KONG_SHA256=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Fri, 22 Apr 2022 04:02:04 GMT
# ARGS: KONG_SHA256=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:02:05 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:02:05 GMT
USER kong
# Fri, 22 Apr 2022 04:02:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:02:05 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:02:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:02:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:02:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f143a86548988add2722c52d2f96f24eeef7e805e5e3ef08d1a1f798ed22fb`  
		Last Modified: Fri, 22 Apr 2022 04:05:16 GMT  
		Size: 74.5 MB (74523371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363b17a0055540de2963a7b38cc39c1d41229d331039536dfe8d0bfd16490175`  
		Last Modified: Fri, 22 Apr 2022 04:05:04 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7`

```console
$ docker pull kong@sha256:4dfe51c0cb836192982dc712c37812c491995cd7b3694d196391f303fc54e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7` - linux; amd64

```console
$ docker pull kong@sha256:c0181f30d526cd839045da3c1f8de9eedd3349ada68cbf6a6bfcec0d563f4461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4896b6c8b9c3f39159184c8b8bbe6dca33cd854f8ff6782d8fa3a0cb6928eb3`
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
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 19:32:08 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:09 GMT
USER kong
# Tue, 12 Apr 2022 19:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:10 GMT
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
	-	`sha256:8d565044977d85c458ac0b142bcd82fbc325e637602315e9817d6b4ec7c9b666`  
		Last Modified: Tue, 12 Apr 2022 19:34:57 GMT  
		Size: 47.3 MB (47305777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b549f27ad073929c3f594f4b83ef3334ace38c2175b39ca52783c23b0f825`  
		Last Modified: Tue, 12 Apr 2022 19:34:49 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f3bc86efee406011153e7acdba5309956ad3c04a526e6d793965454ec09fd35c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e65c552d7762c16f5a4ed65c0b8239113c4fe26c0d8737539412b9418db7b`
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
# Tue, 12 Apr 2022 20:01:32 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:33 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:34 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 20:01:35 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 20:01:44 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:01:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:01:45 GMT
USER kong
# Tue, 12 Apr 2022 20:01:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:01:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:01:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:01:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:01:50 GMT
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
	-	`sha256:fc39d004f3484e0c617d28bfcc3b54061de5edd6e0e17b49a5e971559293cd08`  
		Last Modified: Tue, 12 Apr 2022 20:11:35 GMT  
		Size: 46.8 MB (46806935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694b4ff209cd89703c3efd09e664c43367dc9a4e9d6fe83fa7fbfc578126ed6c`  
		Last Modified: Tue, 12 Apr 2022 20:11:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7-ubuntu`

```console
$ docker pull kong@sha256:ed51c6ee5b85f6b6c9bf2eafaf73cb9379571af65ec0ba033c5efebd73ffe1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b3195761dac9e3a655e9ff35d2bce95616172db9837a604e52afbcc520ff8311
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128080327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2844420e8b1dec6790171b07d84d99d71848d17d9431ad10b07345f8857f66`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 04:00:44 GMT
ARG KONG_VERSION=2.7.2
# Fri, 22 Apr 2022 04:00:45 GMT
ENV KONG_VERSION=2.7.2
# Fri, 22 Apr 2022 04:00:45 GMT
ARG KONG_SHA256=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Fri, 22 Apr 2022 04:01:05 GMT
# ARGS: KONG_SHA256=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:01:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:01:06 GMT
USER kong
# Fri, 22 Apr 2022 04:01:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:01:06 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:01:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:01:06 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:01:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bcd59d26685dbbda09228026a40b8eb4f7e2928b8d40aed7ecd87b261580`  
		Last Modified: Fri, 22 Apr 2022 04:04:33 GMT  
		Size: 74.4 MB (74431486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dc2baf828aeb116cc3cc35e07ef1491af65609ae41b19df143bababf9d611c`  
		Last Modified: Fri, 22 Apr 2022 04:04:21 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.1`

```console
$ docker pull kong@sha256:cceaaccdc162b184490a963558251e4d0b943b124f91afd60c039eacb2a6daeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.1` - linux; amd64

```console
$ docker pull kong@sha256:1c16b62bbac29d34bb9d98b2c4086ddb5a7c4cb3f5894c49795ac937cd41212d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50072135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6a1882af7ab659ee01f9b685778fef813cee85a7cebbe4a830c75b881d585b`
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
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 07:18:26 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:26 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:26 GMT
USER kong
# Tue, 05 Apr 2022 07:18:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:27 GMT
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
	-	`sha256:96d4b98a2b936a3436c0d2da9470c9219252bfc027f7f9bb020b409209f7d8ea`  
		Last Modified: Tue, 05 Apr 2022 07:19:56 GMT  
		Size: 47.3 MB (47256562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73e510ff864bb33d132ecc03600e597b82440a30c0982c3af7020b51899b2bc`  
		Last Modified: Tue, 05 Apr 2022 07:19:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:aa319cc291ab93f3439ab314de844bf4372615469fe7882c052c09e4f03be863
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49481579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a5459f176100a3049e86076a607792a1785517d4940a00bb90d99ed5bcc0f8`
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
# Tue, 05 Apr 2022 14:23:50 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:51 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:52 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 14:23:53 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 14:24:08 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:24:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:24:09 GMT
USER kong
# Tue, 05 Apr 2022 14:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:24:11 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:24:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:24:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:24:14 GMT
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
	-	`sha256:2d0d3010a5a0e66ff16384f855ef03ac57bd485603a15c2f679080e896c3eaae`  
		Last Modified: Tue, 05 Apr 2022 14:31:23 GMT  
		Size: 46.8 MB (46764090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8130dd0a7ba94337ce11c52ef6005a98a02c1200e2f85509a4777c4ee76664`  
		Last Modified: Tue, 05 Apr 2022 14:31:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.1-alpine`

```console
$ docker pull kong@sha256:cceaaccdc162b184490a963558251e4d0b943b124f91afd60c039eacb2a6daeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:1c16b62bbac29d34bb9d98b2c4086ddb5a7c4cb3f5894c49795ac937cd41212d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50072135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6a1882af7ab659ee01f9b685778fef813cee85a7cebbe4a830c75b881d585b`
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
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 07:18:26 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:26 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:26 GMT
USER kong
# Tue, 05 Apr 2022 07:18:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:27 GMT
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
	-	`sha256:96d4b98a2b936a3436c0d2da9470c9219252bfc027f7f9bb020b409209f7d8ea`  
		Last Modified: Tue, 05 Apr 2022 07:19:56 GMT  
		Size: 47.3 MB (47256562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73e510ff864bb33d132ecc03600e597b82440a30c0982c3af7020b51899b2bc`  
		Last Modified: Tue, 05 Apr 2022 07:19:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:aa319cc291ab93f3439ab314de844bf4372615469fe7882c052c09e4f03be863
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49481579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a5459f176100a3049e86076a607792a1785517d4940a00bb90d99ed5bcc0f8`
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
# Tue, 05 Apr 2022 14:23:50 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:51 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:52 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 14:23:53 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 14:24:08 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:24:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:24:09 GMT
USER kong
# Tue, 05 Apr 2022 14:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:24:11 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:24:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:24:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:24:14 GMT
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
	-	`sha256:2d0d3010a5a0e66ff16384f855ef03ac57bd485603a15c2f679080e896c3eaae`  
		Last Modified: Tue, 05 Apr 2022 14:31:23 GMT  
		Size: 46.8 MB (46764090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8130dd0a7ba94337ce11c52ef6005a98a02c1200e2f85509a4777c4ee76664`  
		Last Modified: Tue, 05 Apr 2022 14:31:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.1-ubuntu`

```console
$ docker pull kong@sha256:5cc77aeb1634a4af3cc2a0fcc2e553ee868a772c5e4693988715b34fa4e44c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:06a2fd897c501635215bfd41e01a951a9859cd412aef04440593de472e1faf19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127992225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eede288ec5e338a5a9a48efa1b5e1aa84d3043a02ed0dd15badfecc3d68e1361`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 04:01:14 GMT
ARG KONG_VERSION=2.7.1
# Fri, 22 Apr 2022 04:01:14 GMT
ENV KONG_VERSION=2.7.1
# Fri, 22 Apr 2022 04:01:14 GMT
ARG KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
# Fri, 22 Apr 2022 04:01:34 GMT
# ARGS: KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:01:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:01:36 GMT
USER kong
# Fri, 22 Apr 2022 04:01:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:01:36 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:01:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:01:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:01:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de8890c48dcb9a2670c154affb06e44f5bb31818527a546687a6243d7eb812f`  
		Last Modified: Fri, 22 Apr 2022 04:04:56 GMT  
		Size: 74.3 MB (74343384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38245f56fac6d74c4128461997cda356c945cad51bd6293e072851c246e83be8`  
		Last Modified: Fri, 22 Apr 2022 04:04:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2`

```console
$ docker pull kong@sha256:4dfe51c0cb836192982dc712c37812c491995cd7b3694d196391f303fc54e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2` - linux; amd64

```console
$ docker pull kong@sha256:c0181f30d526cd839045da3c1f8de9eedd3349ada68cbf6a6bfcec0d563f4461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4896b6c8b9c3f39159184c8b8bbe6dca33cd854f8ff6782d8fa3a0cb6928eb3`
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
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 19:32:08 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:09 GMT
USER kong
# Tue, 12 Apr 2022 19:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:10 GMT
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
	-	`sha256:8d565044977d85c458ac0b142bcd82fbc325e637602315e9817d6b4ec7c9b666`  
		Last Modified: Tue, 12 Apr 2022 19:34:57 GMT  
		Size: 47.3 MB (47305777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b549f27ad073929c3f594f4b83ef3334ace38c2175b39ca52783c23b0f825`  
		Last Modified: Tue, 12 Apr 2022 19:34:49 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f3bc86efee406011153e7acdba5309956ad3c04a526e6d793965454ec09fd35c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e65c552d7762c16f5a4ed65c0b8239113c4fe26c0d8737539412b9418db7b`
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
# Tue, 12 Apr 2022 20:01:32 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:33 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:34 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 20:01:35 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 20:01:44 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:01:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:01:45 GMT
USER kong
# Tue, 12 Apr 2022 20:01:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:01:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:01:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:01:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:01:50 GMT
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
	-	`sha256:fc39d004f3484e0c617d28bfcc3b54061de5edd6e0e17b49a5e971559293cd08`  
		Last Modified: Tue, 12 Apr 2022 20:11:35 GMT  
		Size: 46.8 MB (46806935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694b4ff209cd89703c3efd09e664c43367dc9a4e9d6fe83fa7fbfc578126ed6c`  
		Last Modified: Tue, 12 Apr 2022 20:11:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-alpine`

```console
$ docker pull kong@sha256:4dfe51c0cb836192982dc712c37812c491995cd7b3694d196391f303fc54e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:c0181f30d526cd839045da3c1f8de9eedd3349ada68cbf6a6bfcec0d563f4461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4896b6c8b9c3f39159184c8b8bbe6dca33cd854f8ff6782d8fa3a0cb6928eb3`
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
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 19:32:08 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:09 GMT
USER kong
# Tue, 12 Apr 2022 19:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:10 GMT
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
	-	`sha256:8d565044977d85c458ac0b142bcd82fbc325e637602315e9817d6b4ec7c9b666`  
		Last Modified: Tue, 12 Apr 2022 19:34:57 GMT  
		Size: 47.3 MB (47305777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b549f27ad073929c3f594f4b83ef3334ace38c2175b39ca52783c23b0f825`  
		Last Modified: Tue, 12 Apr 2022 19:34:49 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f3bc86efee406011153e7acdba5309956ad3c04a526e6d793965454ec09fd35c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e65c552d7762c16f5a4ed65c0b8239113c4fe26c0d8737539412b9418db7b`
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
# Tue, 12 Apr 2022 20:01:32 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:33 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:34 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 20:01:35 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 20:01:44 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:01:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:01:45 GMT
USER kong
# Tue, 12 Apr 2022 20:01:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:01:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:01:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:01:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:01:50 GMT
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
	-	`sha256:fc39d004f3484e0c617d28bfcc3b54061de5edd6e0e17b49a5e971559293cd08`  
		Last Modified: Tue, 12 Apr 2022 20:11:35 GMT  
		Size: 46.8 MB (46806935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694b4ff209cd89703c3efd09e664c43367dc9a4e9d6fe83fa7fbfc578126ed6c`  
		Last Modified: Tue, 12 Apr 2022 20:11:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-ubuntu`

```console
$ docker pull kong@sha256:ed51c6ee5b85f6b6c9bf2eafaf73cb9379571af65ec0ba033c5efebd73ffe1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b3195761dac9e3a655e9ff35d2bce95616172db9837a604e52afbcc520ff8311
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128080327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2844420e8b1dec6790171b07d84d99d71848d17d9431ad10b07345f8857f66`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 04:00:44 GMT
ARG KONG_VERSION=2.7.2
# Fri, 22 Apr 2022 04:00:45 GMT
ENV KONG_VERSION=2.7.2
# Fri, 22 Apr 2022 04:00:45 GMT
ARG KONG_SHA256=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Fri, 22 Apr 2022 04:01:05 GMT
# ARGS: KONG_SHA256=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:01:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:01:06 GMT
USER kong
# Fri, 22 Apr 2022 04:01:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:01:06 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:01:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:01:06 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:01:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bcd59d26685dbbda09228026a40b8eb4f7e2928b8d40aed7ecd87b261580`  
		Last Modified: Fri, 22 Apr 2022 04:04:33 GMT  
		Size: 74.4 MB (74431486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dc2baf828aeb116cc3cc35e07ef1491af65609ae41b19df143bababf9d611c`  
		Last Modified: Fri, 22 Apr 2022 04:04:21 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

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

### `kong:2.8` - linux; arm64 variant v8

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

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:2063d5f746c5053e343f4bf71ce52a4d2300a05275222f38473efcd6924ad1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5b8d598910fb33633e5812acbd0e71a94fa64f0804486eeda38bacf4263e2f9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121220087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b0c1de96517511a66943b8b2e3a96ae69f8c5d72fa757e249e9fe97c2c198`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 03:59:45 GMT
ARG KONG_VERSION=2.8.1
# Fri, 22 Apr 2022 03:59:45 GMT
ENV KONG_VERSION=2.8.1
# Fri, 22 Apr 2022 03:59:45 GMT
ARG KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Fri, 22 Apr 2022 04:00:12 GMT
# ARGS: KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:00:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:00:13 GMT
USER kong
# Fri, 22 Apr 2022 04:00:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:00:13 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:00:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:00:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:00:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03688c94d0e8dcf709c2aa2ac95a322a69d76d13347fa679d4fdb8aad7e46fd8`  
		Last Modified: Fri, 22 Apr 2022 04:03:47 GMT  
		Size: 67.6 MB (67571246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399b06c2e86700cba85e5dda72be8719dacaee8e960c005d77ea1d988ab21a4`  
		Last Modified: Fri, 22 Apr 2022 04:03:36 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.0`

```console
$ docker pull kong@sha256:92e69c043806c7a77f07b3afa23335bd462fcfe4bcc6646b42527ae2e3682177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.0` - linux; amd64

```console
$ docker pull kong@sha256:80ab9ea850626def46452d984e32d8a6cba057842e3002e03b83eabbf3b3e983
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49114128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abd56e893359a729325103065a1f6c2e004dec25e2ffc382016551372b6707`
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
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 07:18:12 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:13 GMT
USER kong
# Tue, 05 Apr 2022 07:18:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:13 GMT
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
	-	`sha256:05c1f4c755850a2adc30b8cc2b020bfbee49e1a10fe126b299cfd80ffed685be`  
		Last Modified: Tue, 05 Apr 2022 07:19:30 GMT  
		Size: 46.3 MB (46298555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f270dea85947274c1da7de384551b7ab5514066ec071ab3d0ac1ca12004290`  
		Last Modified: Tue, 05 Apr 2022 07:19:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a1b94982b50727d67b57988efb863e3738e28f8f62851f5c0a8f4c8374476ed2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48306718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890c0a81ce116131f054213f59d76846afd1b9efd9893da6c58d37501d4a10c`
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
# Tue, 05 Apr 2022 14:21:22 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:23 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:24 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 14:21:25 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 14:21:43 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:21:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:21:44 GMT
USER kong
# Tue, 05 Apr 2022 14:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:21:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:21:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:21:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:21:49 GMT
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
	-	`sha256:5ab132370421ab09a7865a3492f2060ba102f456f0572e0b574d527ad0dd8f67`  
		Last Modified: Tue, 05 Apr 2022 14:30:34 GMT  
		Size: 45.6 MB (45589229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ab581ead9fa3c47fa83014394d89503e845d302567c5fe34b3282d2c15f90`  
		Last Modified: Tue, 05 Apr 2022 14:30:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.0-alpine`

```console
$ docker pull kong@sha256:92e69c043806c7a77f07b3afa23335bd462fcfe4bcc6646b42527ae2e3682177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:80ab9ea850626def46452d984e32d8a6cba057842e3002e03b83eabbf3b3e983
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49114128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abd56e893359a729325103065a1f6c2e004dec25e2ffc382016551372b6707`
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
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 07:18:12 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:13 GMT
USER kong
# Tue, 05 Apr 2022 07:18:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:13 GMT
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
	-	`sha256:05c1f4c755850a2adc30b8cc2b020bfbee49e1a10fe126b299cfd80ffed685be`  
		Last Modified: Tue, 05 Apr 2022 07:19:30 GMT  
		Size: 46.3 MB (46298555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f270dea85947274c1da7de384551b7ab5514066ec071ab3d0ac1ca12004290`  
		Last Modified: Tue, 05 Apr 2022 07:19:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a1b94982b50727d67b57988efb863e3738e28f8f62851f5c0a8f4c8374476ed2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48306718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890c0a81ce116131f054213f59d76846afd1b9efd9893da6c58d37501d4a10c`
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
# Tue, 05 Apr 2022 14:21:22 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:23 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:24 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 14:21:25 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 14:21:43 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:21:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:21:44 GMT
USER kong
# Tue, 05 Apr 2022 14:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:21:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:21:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:21:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:21:49 GMT
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
	-	`sha256:5ab132370421ab09a7865a3492f2060ba102f456f0572e0b574d527ad0dd8f67`  
		Last Modified: Tue, 05 Apr 2022 14:30:34 GMT  
		Size: 45.6 MB (45589229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ab581ead9fa3c47fa83014394d89503e845d302567c5fe34b3282d2c15f90`  
		Last Modified: Tue, 05 Apr 2022 14:30:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.0-ubuntu`

```console
$ docker pull kong@sha256:9cfea31b71ef258894b7d3387a1d7a08981c91d32d2591cbc298aec5b58b0125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:46ca9e9d75e229b8680c7a8a5c5f93e647f1207ffbcce4e65dc95c24786bf65f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121217707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba02fbbf5d3714504da03db76f60fde862dfba0e9d5cedd847791ef097299a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 04:00:19 GMT
ARG KONG_VERSION=2.8.0
# Fri, 22 Apr 2022 04:00:20 GMT
ENV KONG_VERSION=2.8.0
# Fri, 22 Apr 2022 04:00:20 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Fri, 22 Apr 2022 04:00:39 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:00:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:00:40 GMT
USER kong
# Fri, 22 Apr 2022 04:00:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:00:40 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:00:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:00:40 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:00:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d186aa33e28989885b3498ed95f4d49da24522fd106792d6438dbad00f823f73`  
		Last Modified: Fri, 22 Apr 2022 04:04:12 GMT  
		Size: 67.6 MB (67568867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ef51facb9f4198ff0e9c5aa494e1cf9e5b1380aa2cc40a3ac25a3d31fb24d9`  
		Last Modified: Fri, 22 Apr 2022 04:04:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1` - linux; amd64

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

### `kong:2.8.1` - linux; arm64 variant v8

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

## `kong:2.8.1-alpine`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-alpine` - linux; amd64

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

### `kong:2.8.1-alpine` - linux; arm64 variant v8

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

## `kong:2.8.1-ubuntu`

```console
$ docker pull kong@sha256:2063d5f746c5053e343f4bf71ce52a4d2300a05275222f38473efcd6924ad1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5b8d598910fb33633e5812acbd0e71a94fa64f0804486eeda38bacf4263e2f9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121220087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b0c1de96517511a66943b8b2e3a96ae69f8c5d72fa757e249e9fe97c2c198`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 03:59:45 GMT
ARG KONG_VERSION=2.8.1
# Fri, 22 Apr 2022 03:59:45 GMT
ENV KONG_VERSION=2.8.1
# Fri, 22 Apr 2022 03:59:45 GMT
ARG KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Fri, 22 Apr 2022 04:00:12 GMT
# ARGS: KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:00:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:00:13 GMT
USER kong
# Fri, 22 Apr 2022 04:00:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:00:13 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:00:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:00:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:00:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03688c94d0e8dcf709c2aa2ac95a322a69d76d13347fa679d4fdb8aad7e46fd8`  
		Last Modified: Fri, 22 Apr 2022 04:03:47 GMT  
		Size: 67.6 MB (67571246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399b06c2e86700cba85e5dda72be8719dacaee8e960c005d77ea1d988ab21a4`  
		Last Modified: Fri, 22 Apr 2022 04:03:36 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

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

### `kong:alpine` - linux; arm64 variant v8

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

## `kong:ubuntu`

```console
$ docker pull kong@sha256:cc8742114e42410c9f1f4e8362d06486f719e782bcde3d9846a386ff47a5db32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5b8d598910fb33633e5812acbd0e71a94fa64f0804486eeda38bacf4263e2f9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121220087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88b0c1de96517511a66943b8b2e3a96ae69f8c5d72fa757e249e9fe97c2c198`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:59:44 GMT
ARG ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ENV ASSET=ce
# Fri, 22 Apr 2022 03:59:44 GMT
ARG EE_PORTS
# Fri, 22 Apr 2022 03:59:45 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 22 Apr 2022 03:59:45 GMT
ARG KONG_VERSION=2.8.1
# Fri, 22 Apr 2022 03:59:45 GMT
ENV KONG_VERSION=2.8.1
# Fri, 22 Apr 2022 03:59:45 GMT
ARG KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Fri, 22 Apr 2022 04:00:12 GMT
# ARGS: KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 22 Apr 2022 04:00:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 22 Apr 2022 04:00:13 GMT
USER kong
# Fri, 22 Apr 2022 04:00:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 Apr 2022 04:00:13 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 22 Apr 2022 04:00:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 Apr 2022 04:00:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 22 Apr 2022 04:00:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20014f8d88b07eebd92858d3ae14e27c6aa299e94a701f06a84e5adde69055d7`  
		Last Modified: Fri, 22 Apr 2022 04:03:37 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03688c94d0e8dcf709c2aa2ac95a322a69d76d13347fa679d4fdb8aad7e46fd8`  
		Last Modified: Fri, 22 Apr 2022 04:03:47 GMT  
		Size: 67.6 MB (67571246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399b06c2e86700cba85e5dda72be8719dacaee8e960c005d77ea1d988ab21a4`  
		Last Modified: Fri, 22 Apr 2022 04:03:36 GMT  
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
