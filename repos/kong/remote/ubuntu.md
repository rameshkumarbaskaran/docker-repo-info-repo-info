## `kong:ubuntu`

```console
$ docker pull kong@sha256:544c454624e811be0e3288d573920266188b5ddc4890aa490b29b1b78255b119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:74fd7d02fc80426128220c844b649ee80e078e0dcb4b2684c06b83636f4492e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81324591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ac5c3d6929b19e745f738a7e38ffe7aac08c148cc07f5778b221c9c276ed78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:02:20 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 16 Jun 2023 03:02:20 GMT
ARG ASSET=ce
# Fri, 16 Jun 2023 03:02:20 GMT
ENV ASSET=ce
# Fri, 16 Jun 2023 03:02:20 GMT
ARG EE_PORTS
# Fri, 16 Jun 2023 03:02:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 16 Jun 2023 03:02:20 GMT
ARG KONG_VERSION=3.3.0
# Fri, 16 Jun 2023 03:02:20 GMT
ENV KONG_VERSION=3.3.0
# Fri, 16 Jun 2023 03:02:20 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Fri, 16 Jun 2023 03:02:20 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Fri, 16 Jun 2023 03:03:00 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Jun 2023 03:03:01 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Jun 2023 03:03:01 GMT
USER kong
# Fri, 16 Jun 2023 03:03:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 03:03:01 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Jun 2023 03:03:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jun 2023 03:03:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Jun 2023 03:03:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b770a78ff719726efe345cf12823afe49c4f5dcfdb7c5592748ab9952e0bc087`  
		Last Modified: Fri, 16 Jun 2023 03:05:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d8f511e7f8d6ec0ce9cbb5237ebd5f850a99daf26f983923273a4faf566e0a`  
		Last Modified: Fri, 16 Jun 2023 03:05:07 GMT  
		Size: 50.9 MB (50892272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f2a3e4dd7fc95c394ec37022ac3067a0f4831948c64a4417681a6d38b54a8a`  
		Last Modified: Fri, 16 Jun 2023 03:04:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1af0841022124e34b06deef7223695918912f31bac0d41a5b973b57f235e9f0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75729473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43979f607227bbb2b07e6de8a0352138b806c807dcfc885c007f7d6235c368ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:56:30 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 04 Jul 2023 15:56:30 GMT
ARG ASSET=ce
# Tue, 04 Jul 2023 15:56:30 GMT
ENV ASSET=ce
# Tue, 04 Jul 2023 15:56:31 GMT
ARG EE_PORTS
# Tue, 04 Jul 2023 15:56:31 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Tue, 04 Jul 2023 15:56:31 GMT
ARG KONG_VERSION=3.3.0
# Tue, 04 Jul 2023 15:56:31 GMT
ENV KONG_VERSION=3.3.0
# Tue, 04 Jul 2023 15:56:31 GMT
ARG KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b
# Tue, 04 Jul 2023 15:56:31 GMT
ARG KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
# Tue, 04 Jul 2023 15:56:55 GMT
# ARGS: KONG_AMD64_SHA=e8c5fe8cacf19477d37a3b16375a263183f0c87c9ec217c4ead0c774d286be5b KONG_ARM64_SHA=2d918f7dd1ca5d54a6832cc370892a99af8e39fc4040df66d2d7ca6d97b9a2b5
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 04 Jul 2023 15:56:55 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Tue, 04 Jul 2023 15:56:55 GMT
USER kong
# Tue, 04 Jul 2023 15:56:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 15:56:55 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 04 Jul 2023 15:56:55 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Jul 2023 15:56:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 04 Jul 2023 15:56:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323749330ae28b00c28d5d9426a6340ac8c0950f884d5f86035845592177af50`  
		Last Modified: Tue, 04 Jul 2023 15:58:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0838f7579b4383b8de9c9ba94ea92f5e8bf54501aad19ff3c7b20a69d3e9601c`  
		Last Modified: Tue, 04 Jul 2023 15:58:33 GMT  
		Size: 47.3 MB (47337178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86236cf6ed5d8a29939463122de34686c5333330b978ec314bb8718c4bf9f92d`  
		Last Modified: Tue, 04 Jul 2023 15:58:27 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
