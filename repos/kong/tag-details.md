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
$ docker pull kong@sha256:acb0a9a375107804d109437760f5fbb4bb467f24d9f9988652e9458472f53df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:6896f87b90dcea49ee7009a9963a709e5644ebf0dff8491d2c010bf7fab6a974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b114251eef2a2e43dbd58ea78009aa1eee554e03aad3399ccd64dac711f6437`
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
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:26 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:26 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:35 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:36 GMT
USER kong
# Sat, 13 Nov 2021 05:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:37 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:37 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:38 GMT
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
	-	`sha256:ccc7ab7edbafff55c804c295704914b38324636bc651035e4f405b24f4b86948`  
		Last Modified: Sat, 13 Nov 2021 05:51:23 GMT  
		Size: 47.0 MB (47002560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a49a9faa0e6e6630ec2942c9320fa92d94e2e7f5be3ed6cb179adc2cdf39e`  
		Last Modified: Sat, 13 Nov 2021 05:51:14 GMT  
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
$ docker pull kong@sha256:30e4483e5e21c703f40768765a40710bbcd50cdeb039c0f047eeba422d11979f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:abaab2e18ad168fa84085df49782271e4daf52caf26b6a6adeee800eab36ae8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128043847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b343db80e8ea3289caae03b1820b5b0ae0fa21d9c527bc88a6abf4e475884b72`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 01:25:11 GMT
ARG ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ENV ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ARG EE_PORTS
# Fri, 04 Mar 2022 01:25:12 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 04 Mar 2022 01:26:43 GMT
ARG KONG_VERSION=2.5.1
# Fri, 04 Mar 2022 01:26:43 GMT
ENV KONG_VERSION=2.5.1
# Fri, 04 Mar 2022 01:27:02 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 04 Mar 2022 01:27:03 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 04 Mar 2022 01:27:03 GMT
USER kong
# Fri, 04 Mar 2022 01:27:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Mar 2022 01:27:03 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 04 Mar 2022 01:27:03 GMT
STOPSIGNAL SIGQUIT
# Fri, 04 Mar 2022 01:27:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 04 Mar 2022 01:27:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55825048bbe2e3a3aaf348ca4bdda392657727fa832c89d90ecd145f00e`  
		Last Modified: Fri, 04 Mar 2022 01:27:33 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4b5820a89cd6e938dcf21551bbb7db37eeee6133cd4a7d5038f0620ab39b0b`  
		Last Modified: Fri, 04 Mar 2022 01:28:53 GMT  
		Size: 74.4 MB (74395247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ab8a9270d64fc2621a9107b71c4e5b2cf8ddbf8c690fc871157a644aef0790`  
		Last Modified: Fri, 04 Mar 2022 01:28:41 GMT  
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
$ docker pull kong@sha256:acb0a9a375107804d109437760f5fbb4bb467f24d9f9988652e9458472f53df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1` - linux; amd64

```console
$ docker pull kong@sha256:6896f87b90dcea49ee7009a9963a709e5644ebf0dff8491d2c010bf7fab6a974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b114251eef2a2e43dbd58ea78009aa1eee554e03aad3399ccd64dac711f6437`
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
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:26 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:26 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:35 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:36 GMT
USER kong
# Sat, 13 Nov 2021 05:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:37 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:37 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:38 GMT
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
	-	`sha256:ccc7ab7edbafff55c804c295704914b38324636bc651035e4f405b24f4b86948`  
		Last Modified: Sat, 13 Nov 2021 05:51:23 GMT  
		Size: 47.0 MB (47002560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a49a9faa0e6e6630ec2942c9320fa92d94e2e7f5be3ed6cb179adc2cdf39e`  
		Last Modified: Sat, 13 Nov 2021 05:51:14 GMT  
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
$ docker pull kong@sha256:acb0a9a375107804d109437760f5fbb4bb467f24d9f9988652e9458472f53df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:6896f87b90dcea49ee7009a9963a709e5644ebf0dff8491d2c010bf7fab6a974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b114251eef2a2e43dbd58ea78009aa1eee554e03aad3399ccd64dac711f6437`
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
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:26 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:26 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:35 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:36 GMT
USER kong
# Sat, 13 Nov 2021 05:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:37 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:37 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:38 GMT
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
	-	`sha256:ccc7ab7edbafff55c804c295704914b38324636bc651035e4f405b24f4b86948`  
		Last Modified: Sat, 13 Nov 2021 05:51:23 GMT  
		Size: 47.0 MB (47002560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a49a9faa0e6e6630ec2942c9320fa92d94e2e7f5be3ed6cb179adc2cdf39e`  
		Last Modified: Sat, 13 Nov 2021 05:51:14 GMT  
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
$ docker pull kong@sha256:0e9af7c7b689043349974dcf0465e62aa9032f5891a67dfa0383dfce5ca9502a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.5.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:abaab2e18ad168fa84085df49782271e4daf52caf26b6a6adeee800eab36ae8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128043847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b343db80e8ea3289caae03b1820b5b0ae0fa21d9c527bc88a6abf4e475884b72`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 01:25:11 GMT
ARG ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ENV ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ARG EE_PORTS
# Fri, 04 Mar 2022 01:25:12 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 04 Mar 2022 01:26:43 GMT
ARG KONG_VERSION=2.5.1
# Fri, 04 Mar 2022 01:26:43 GMT
ENV KONG_VERSION=2.5.1
# Fri, 04 Mar 2022 01:27:02 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 04 Mar 2022 01:27:03 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 04 Mar 2022 01:27:03 GMT
USER kong
# Fri, 04 Mar 2022 01:27:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Mar 2022 01:27:03 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 04 Mar 2022 01:27:03 GMT
STOPSIGNAL SIGQUIT
# Fri, 04 Mar 2022 01:27:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 04 Mar 2022 01:27:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55825048bbe2e3a3aaf348ca4bdda392657727fa832c89d90ecd145f00e`  
		Last Modified: Fri, 04 Mar 2022 01:27:33 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4b5820a89cd6e938dcf21551bbb7db37eeee6133cd4a7d5038f0620ab39b0b`  
		Last Modified: Fri, 04 Mar 2022 01:28:53 GMT  
		Size: 74.4 MB (74395247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ab8a9270d64fc2621a9107b71c4e5b2cf8ddbf8c690fc871157a644aef0790`  
		Last Modified: Fri, 04 Mar 2022 01:28:41 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:49ad096ff7e394239187d7915463ff893468f53c1a252460d58b51d5adb3b6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

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
$ docker pull kong@sha256:c3794c31f96a81de12683aab31c6ae77f449abaa741918233f51ab957615e341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7b641c4e9fdfa86df077ba556231a591875a0ff479a6fa2d5bfa5996da68be4e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128086179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df93bc7369abb6cce24cf92d283c530c2a1b74f53908b48f9801533dea940b9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 01:25:11 GMT
ARG ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ENV ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ARG EE_PORTS
# Fri, 04 Mar 2022 01:25:12 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 04 Mar 2022 01:26:18 GMT
ARG KONG_VERSION=2.6.0
# Fri, 04 Mar 2022 01:26:18 GMT
ENV KONG_VERSION=2.6.0
# Fri, 04 Mar 2022 01:26:37 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 04 Mar 2022 01:26:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 04 Mar 2022 01:26:38 GMT
USER kong
# Fri, 04 Mar 2022 01:26:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Mar 2022 01:26:38 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 04 Mar 2022 01:26:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 04 Mar 2022 01:26:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 04 Mar 2022 01:26:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55825048bbe2e3a3aaf348ca4bdda392657727fa832c89d90ecd145f00e`  
		Last Modified: Fri, 04 Mar 2022 01:27:33 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc383fa995e784b9752055712e55b9f799fbe2ad44a4c29349bb3d3ed102028`  
		Last Modified: Fri, 04 Mar 2022 01:28:31 GMT  
		Size: 74.4 MB (74437579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5e99a077db63bef924eea4d3a983f63f90042effdd4b9af017a2d008d8b2c`  
		Last Modified: Fri, 04 Mar 2022 01:28:19 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0`

```console
$ docker pull kong@sha256:49ad096ff7e394239187d7915463ff893468f53c1a252460d58b51d5adb3b6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0` - linux; amd64

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
$ docker pull kong@sha256:49ad096ff7e394239187d7915463ff893468f53c1a252460d58b51d5adb3b6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0-alpine` - linux; amd64

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
$ docker pull kong@sha256:c3794c31f96a81de12683aab31c6ae77f449abaa741918233f51ab957615e341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7b641c4e9fdfa86df077ba556231a591875a0ff479a6fa2d5bfa5996da68be4e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128086179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df93bc7369abb6cce24cf92d283c530c2a1b74f53908b48f9801533dea940b9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 01:25:11 GMT
ARG ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ENV ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ARG EE_PORTS
# Fri, 04 Mar 2022 01:25:12 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 04 Mar 2022 01:26:18 GMT
ARG KONG_VERSION=2.6.0
# Fri, 04 Mar 2022 01:26:18 GMT
ENV KONG_VERSION=2.6.0
# Fri, 04 Mar 2022 01:26:37 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 04 Mar 2022 01:26:38 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 04 Mar 2022 01:26:38 GMT
USER kong
# Fri, 04 Mar 2022 01:26:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Mar 2022 01:26:38 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 04 Mar 2022 01:26:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 04 Mar 2022 01:26:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 04 Mar 2022 01:26:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55825048bbe2e3a3aaf348ca4bdda392657727fa832c89d90ecd145f00e`  
		Last Modified: Fri, 04 Mar 2022 01:27:33 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc383fa995e784b9752055712e55b9f799fbe2ad44a4c29349bb3d3ed102028`  
		Last Modified: Fri, 04 Mar 2022 01:28:31 GMT  
		Size: 74.4 MB (74437579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5e99a077db63bef924eea4d3a983f63f90042effdd4b9af017a2d008d8b2c`  
		Last Modified: Fri, 04 Mar 2022 01:28:19 GMT  
		Size: 880.0 B  
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
$ docker pull kong@sha256:3d68f930259ca358ef644a5d23e6eceb924e8f2e2f1d6c9f7cbd49309df09d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:78b1b71022fcd7cabe0499f0f58d04d2e8e786860b32cd444cdd886e00673498
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127997333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2af05bb883e3c169e143a43fe43b532e7ed18648a888fc2fe0f82cb9482ff1b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 01:25:11 GMT
ARG ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ENV ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ARG EE_PORTS
# Fri, 04 Mar 2022 01:25:12 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 04 Mar 2022 01:25:53 GMT
ARG KONG_VERSION=2.7.1
# Fri, 04 Mar 2022 01:25:53 GMT
ENV KONG_VERSION=2.7.1
# Fri, 04 Mar 2022 01:25:53 GMT
ARG KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
# Fri, 04 Mar 2022 01:26:12 GMT
# ARGS: KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 04 Mar 2022 01:26:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 04 Mar 2022 01:26:13 GMT
USER kong
# Fri, 04 Mar 2022 01:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Mar 2022 01:26:13 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 04 Mar 2022 01:26:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 04 Mar 2022 01:26:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 04 Mar 2022 01:26:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55825048bbe2e3a3aaf348ca4bdda392657727fa832c89d90ecd145f00e`  
		Last Modified: Fri, 04 Mar 2022 01:27:33 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacb11082c9934eba904946fb83be7b64ded39d9823029a9a8bdde191538981`  
		Last Modified: Fri, 04 Mar 2022 01:28:08 GMT  
		Size: 74.3 MB (74348732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4d1b21e283a79ac34e3fa9c25f136af3b082ae81de09029bfe030ad5c36ff`  
		Last Modified: Fri, 04 Mar 2022 01:27:56 GMT  
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
$ docker pull kong@sha256:3d68f930259ca358ef644a5d23e6eceb924e8f2e2f1d6c9f7cbd49309df09d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:78b1b71022fcd7cabe0499f0f58d04d2e8e786860b32cd444cdd886e00673498
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127997333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2af05bb883e3c169e143a43fe43b532e7ed18648a888fc2fe0f82cb9482ff1b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 01:25:11 GMT
ARG ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ENV ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ARG EE_PORTS
# Fri, 04 Mar 2022 01:25:12 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 04 Mar 2022 01:25:53 GMT
ARG KONG_VERSION=2.7.1
# Fri, 04 Mar 2022 01:25:53 GMT
ENV KONG_VERSION=2.7.1
# Fri, 04 Mar 2022 01:25:53 GMT
ARG KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
# Fri, 04 Mar 2022 01:26:12 GMT
# ARGS: KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 04 Mar 2022 01:26:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 04 Mar 2022 01:26:13 GMT
USER kong
# Fri, 04 Mar 2022 01:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Mar 2022 01:26:13 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 04 Mar 2022 01:26:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 04 Mar 2022 01:26:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 04 Mar 2022 01:26:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55825048bbe2e3a3aaf348ca4bdda392657727fa832c89d90ecd145f00e`  
		Last Modified: Fri, 04 Mar 2022 01:27:33 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacb11082c9934eba904946fb83be7b64ded39d9823029a9a8bdde191538981`  
		Last Modified: Fri, 04 Mar 2022 01:28:08 GMT  
		Size: 74.3 MB (74348732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4d1b21e283a79ac34e3fa9c25f136af3b082ae81de09029bfe030ad5c36ff`  
		Last Modified: Fri, 04 Mar 2022 01:27:56 GMT  
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
$ docker pull kong@sha256:81dbb9e3279771e1b09372673800798710f068a85881576b2a954b183d095ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c07ce75edd42a752677f56f68374f4dc1c6e452124088a94668bc481284f61ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121214294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f88662beb2a57ac62c7c698e49ce82bc9f6714b34ee1611c13e5c09e616273`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 01:25:11 GMT
ARG ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ENV ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ARG EE_PORTS
# Fri, 04 Mar 2022 01:25:12 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 04 Mar 2022 01:25:12 GMT
ARG KONG_VERSION=2.8.0
# Fri, 04 Mar 2022 01:25:12 GMT
ENV KONG_VERSION=2.8.0
# Fri, 04 Mar 2022 01:25:12 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Fri, 04 Mar 2022 01:25:46 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 04 Mar 2022 01:25:47 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 04 Mar 2022 01:25:47 GMT
USER kong
# Fri, 04 Mar 2022 01:25:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Mar 2022 01:25:47 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 04 Mar 2022 01:25:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 04 Mar 2022 01:25:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 04 Mar 2022 01:25:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55825048bbe2e3a3aaf348ca4bdda392657727fa832c89d90ecd145f00e`  
		Last Modified: Fri, 04 Mar 2022 01:27:33 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690d16d2a3bf0c183932515208479603dade51e734bbdb2b7145eec5cf5b19ec`  
		Last Modified: Fri, 04 Mar 2022 01:27:43 GMT  
		Size: 67.6 MB (67565694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6e38066a501f159d5839c8e6b507256126dbb3b715949f4f3c382aca480b10`  
		Last Modified: Fri, 04 Mar 2022 01:27:31 GMT  
		Size: 880.0 B  
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
$ docker pull kong@sha256:81dbb9e3279771e1b09372673800798710f068a85881576b2a954b183d095ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c07ce75edd42a752677f56f68374f4dc1c6e452124088a94668bc481284f61ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121214294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f88662beb2a57ac62c7c698e49ce82bc9f6714b34ee1611c13e5c09e616273`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 01:25:11 GMT
ARG ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ENV ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ARG EE_PORTS
# Fri, 04 Mar 2022 01:25:12 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 04 Mar 2022 01:25:12 GMT
ARG KONG_VERSION=2.8.0
# Fri, 04 Mar 2022 01:25:12 GMT
ENV KONG_VERSION=2.8.0
# Fri, 04 Mar 2022 01:25:12 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Fri, 04 Mar 2022 01:25:46 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 04 Mar 2022 01:25:47 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 04 Mar 2022 01:25:47 GMT
USER kong
# Fri, 04 Mar 2022 01:25:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Mar 2022 01:25:47 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 04 Mar 2022 01:25:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 04 Mar 2022 01:25:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 04 Mar 2022 01:25:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55825048bbe2e3a3aaf348ca4bdda392657727fa832c89d90ecd145f00e`  
		Last Modified: Fri, 04 Mar 2022 01:27:33 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690d16d2a3bf0c183932515208479603dade51e734bbdb2b7145eec5cf5b19ec`  
		Last Modified: Fri, 04 Mar 2022 01:27:43 GMT  
		Size: 67.6 MB (67565694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6e38066a501f159d5839c8e6b507256126dbb3b715949f4f3c382aca480b10`  
		Last Modified: Fri, 04 Mar 2022 01:27:31 GMT  
		Size: 880.0 B  
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
$ docker pull kong@sha256:b09cd18c362def7d5b88314e4551cd4c7ec0211c862ca7f6091df956ea4f382b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c07ce75edd42a752677f56f68374f4dc1c6e452124088a94668bc481284f61ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121214294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f88662beb2a57ac62c7c698e49ce82bc9f6714b34ee1611c13e5c09e616273`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 01:25:11 GMT
ARG ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ENV ASSET=ce
# Fri, 04 Mar 2022 01:25:11 GMT
ARG EE_PORTS
# Fri, 04 Mar 2022 01:25:12 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 04 Mar 2022 01:25:12 GMT
ARG KONG_VERSION=2.8.0
# Fri, 04 Mar 2022 01:25:12 GMT
ENV KONG_VERSION=2.8.0
# Fri, 04 Mar 2022 01:25:12 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Fri, 04 Mar 2022 01:25:46 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 04 Mar 2022 01:25:47 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 04 Mar 2022 01:25:47 GMT
USER kong
# Fri, 04 Mar 2022 01:25:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Mar 2022 01:25:47 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 04 Mar 2022 01:25:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 04 Mar 2022 01:25:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 04 Mar 2022 01:25:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55825048bbe2e3a3aaf348ca4bdda392657727fa832c89d90ecd145f00e`  
		Last Modified: Fri, 04 Mar 2022 01:27:33 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690d16d2a3bf0c183932515208479603dade51e734bbdb2b7145eec5cf5b19ec`  
		Last Modified: Fri, 04 Mar 2022 01:27:43 GMT  
		Size: 67.6 MB (67565694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6e38066a501f159d5839c8e6b507256126dbb3b715949f4f3c382aca480b10`  
		Last Modified: Fri, 04 Mar 2022 01:27:31 GMT  
		Size: 880.0 B  
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
