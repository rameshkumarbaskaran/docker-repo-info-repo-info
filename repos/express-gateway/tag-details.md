<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `express-gateway`

-	[`express-gateway:1.16.11`](#express-gateway11611)
-	[`express-gateway:1.16.x`](#express-gateway116x)
-	[`express-gateway:1.x`](#express-gateway1x)
-	[`express-gateway:latest`](#express-gatewaylatest)

## `express-gateway:1.16.11`

```console
$ docker pull express-gateway@sha256:301a745e5c9156164ff3b56fd6a4abca1ae4fd1f6ef90912707d93db9881702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:1.16.11` - linux; amd64

```console
$ docker pull express-gateway@sha256:b2c2c32f328db5774e533d775cfee3a168392eb5a1ac8956a2fc4d928fa9e1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40215767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4750d89b8c24f3fec3de71ea88a938aa0a96344bfa99c27ceb3bc2562e9193b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 21:23:29 GMT
ENV NODE_VERSION=12.22.9
# Tue, 11 Jan 2022 21:23:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bda831fbebfc00d12dbbc59b6d3736350d8cfbd495753c725800db10e591eb20"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 21:23:41 GMT
ENV YARN_VERSION=1.22.17
# Wed, 12 Jan 2022 00:13:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 12 Jan 2022 00:13:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:13:25 GMT
CMD ["node"]
# Wed, 12 Jan 2022 00:21:07 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 12 Jan 2022 00:21:07 GMT
ARG EG_VERSION=1.16.11
# Wed, 12 Jan 2022 00:21:40 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 12 Jan 2022 00:21:40 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 00:21:40 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 12 Jan 2022 00:21:41 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 12 Jan 2022 00:21:41 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 12 Jan 2022 00:21:41 GMT
VOLUME [/var/lib/eg]
# Wed, 12 Jan 2022 00:21:41 GMT
EXPOSE 8080 9876
# Wed, 12 Jan 2022 00:21:41 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:21:42 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea1bcfc51681a204ae05c69001c5b7d72bf091d2bfa06f18db72f380ab7494`  
		Last Modified: Wed, 12 Jan 2022 00:18:22 GMT  
		Size: 24.9 MB (24935078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55284a5c72ce1ed6a1c6a6601d67bdabdb0fa7d111921adca44238fdb08c71af`  
		Last Modified: Wed, 12 Jan 2022 00:18:16 GMT  
		Size: 2.4 MB (2367619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9867c49b9ebe6a7af9f0066c7b4fbdd083d658335b83c57c57f368abb43de92`  
		Last Modified: Wed, 12 Jan 2022 00:18:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fed4adb9d69e261ebc708fd9d3eb2892d6d2438d06a99494b7118a03d4c8612`  
		Last Modified: Wed, 12 Jan 2022 00:22:02 GMT  
		Size: 10.1 MB (10093701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b0b1eb8db440077d2b3cd8ffb7687dacf0819c76c05390c41e81d3aa231c88`  
		Last Modified: Wed, 12 Jan 2022 00:21:59 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.11` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:761cea51c7d1d098a65ed31ff9f9502c93bdd23aa9f17214c6ba6fab6967e74a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40076361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e095f6879a7f80a5fd4ebc9e9967a58fbb00a32a2057538cc506678b0b70a81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 22:48:50 GMT
ENV NODE_VERSION=12.22.9
# Tue, 11 Jan 2022 23:06:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bda831fbebfc00d12dbbc59b6d3736350d8cfbd495753c725800db10e591eb20"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 23:06:18 GMT
ENV YARN_VERSION=1.22.17
# Tue, 11 Jan 2022 23:06:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 11 Jan 2022 23:06:25 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 11 Jan 2022 23:06:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jan 2022 23:06:26 GMT
CMD ["node"]
# Wed, 12 Jan 2022 00:36:26 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 12 Jan 2022 00:36:26 GMT
ARG EG_VERSION=1.16.11
# Wed, 12 Jan 2022 00:36:46 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 12 Jan 2022 00:36:47 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 00:36:48 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 12 Jan 2022 00:36:48 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 12 Jan 2022 00:36:49 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 12 Jan 2022 00:36:50 GMT
VOLUME [/var/lib/eg]
# Wed, 12 Jan 2022 00:36:51 GMT
EXPOSE 8080 9876
# Wed, 12 Jan 2022 00:36:53 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:36:54 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9060f367f1180782ca5f4ea561eb558b819462f985f2668562d1b3aa8b46bfdb`  
		Last Modified: Tue, 11 Jan 2022 23:29:32 GMT  
		Size: 24.8 MB (24821785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f579526409f0efbcc848745755ec3dbc748f6e855037f1e709f1d9cdadea5e62`  
		Last Modified: Tue, 11 Jan 2022 23:29:28 GMT  
		Size: 2.4 MB (2439307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2bc6a98cc8a0b0bd450c2c88a6db2f26a9810c044ea9c66acef24ae05a6adf`  
		Last Modified: Tue, 11 Jan 2022 23:29:27 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbf831da352b388d9efa20075d78154468310e5d3763a99fa983ea15c4574e`  
		Last Modified: Wed, 12 Jan 2022 00:37:18 GMT  
		Size: 10.1 MB (10098887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126af8567de32913438641b026f7c72c90ec372b688bbe02a1cbdbb578f4dff1`  
		Last Modified: Wed, 12 Jan 2022 00:37:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.11` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:7b8658ac6172e70175d37d3a35dfcc58d0a1478ff8944f0289deb39955720e80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42500616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ccea382dda64286cf1e6442b00317514697f4fe10347fe29f0262a9cd2eaf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Mon, 03 Jan 2022 20:52:20 GMT
ENV NODE_VERSION=12.22.8
# Mon, 03 Jan 2022 21:10:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="9cc1d120c404d66a62d6e4daaba361e8e1996bdc5b9643f97bbd1241247332df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 03 Jan 2022 21:11:02 GMT
ENV YARN_VERSION=1.22.17
# Mon, 03 Jan 2022 21:11:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 03 Jan 2022 21:11:14 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 03 Jan 2022 21:11:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 21:11:17 GMT
CMD ["node"]
# Mon, 03 Jan 2022 22:31:44 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Mon, 03 Jan 2022 22:31:47 GMT
ARG EG_VERSION=1.16.11
# Mon, 03 Jan 2022 22:32:25 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Mon, 03 Jan 2022 22:32:31 GMT
ENV NODE_ENV=production
# Mon, 03 Jan 2022 22:32:34 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Mon, 03 Jan 2022 22:32:36 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Mon, 03 Jan 2022 22:32:38 GMT
ENV CHOKIDAR_USEPOLLING=true
# Mon, 03 Jan 2022 22:32:42 GMT
VOLUME [/var/lib/eg]
# Mon, 03 Jan 2022 22:32:44 GMT
EXPOSE 8080 9876
# Mon, 03 Jan 2022 22:32:45 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Mon, 03 Jan 2022 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 22:32:50 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd8ae3ce34c1b7eb183bbf0256c324cca8320fbd95714db3073e3c87a025d4`  
		Last Modified: Mon, 03 Jan 2022 21:19:22 GMT  
		Size: 27.2 MB (27152474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb88dcbb6546833e6ff1d90decf1ca584f3d1222966bb3622d8ef26cc30240a`  
		Last Modified: Mon, 03 Jan 2022 21:19:17 GMT  
		Size: 2.4 MB (2439494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e241b4784ab1e6ed8e73c40e765eb635694f16ebb8eb56a5c3a31b8d0c698a89`  
		Last Modified: Mon, 03 Jan 2022 21:19:16 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d143ea5e0b7ab4240374827d452cc0c552e1475922c72ba363e88bbd77ba1c1a`  
		Last Modified: Mon, 03 Jan 2022 22:33:23 GMT  
		Size: 10.1 MB (10092925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fcdf040429b2c88cc60a69a745aea3c425255262d281380ef480bf2546ce`  
		Last Modified: Mon, 03 Jan 2022 22:33:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.11` - linux; s390x

```console
$ docker pull express-gateway@sha256:65ef90c1b4769878961cf3120838bd1a4d172a71c80c7f5cfc55fa445e04494c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39964175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a081214b069709185112015b57d8132bc30db8f911b27c1ac66dd4bc64213bd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Mon, 03 Jan 2022 21:20:28 GMT
ENV NODE_VERSION=12.22.8
# Mon, 03 Jan 2022 21:40:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="9cc1d120c404d66a62d6e4daaba361e8e1996bdc5b9643f97bbd1241247332df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 03 Jan 2022 21:40:59 GMT
ENV YARN_VERSION=1.22.17
# Mon, 03 Jan 2022 21:41:03 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 03 Jan 2022 21:41:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 03 Jan 2022 21:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 21:41:04 GMT
CMD ["node"]
# Mon, 03 Jan 2022 22:25:10 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Mon, 03 Jan 2022 22:25:10 GMT
ARG EG_VERSION=1.16.11
# Mon, 03 Jan 2022 22:25:33 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Mon, 03 Jan 2022 22:25:36 GMT
ENV NODE_ENV=production
# Mon, 03 Jan 2022 22:25:36 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Mon, 03 Jan 2022 22:25:37 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Mon, 03 Jan 2022 22:25:37 GMT
ENV CHOKIDAR_USEPOLLING=true
# Mon, 03 Jan 2022 22:25:37 GMT
VOLUME [/var/lib/eg]
# Mon, 03 Jan 2022 22:25:37 GMT
EXPOSE 8080 9876
# Mon, 03 Jan 2022 22:25:37 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Mon, 03 Jan 2022 22:25:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 22:25:38 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17afc4c4e622a9d3ffec3b18b57875679992dd76ad7da3cd328b8c835477fd0`  
		Last Modified: Mon, 03 Jan 2022 21:48:36 GMT  
		Size: 24.8 MB (24822482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901c31be32d2518467b683d91a3707b8d1aa1a692ce2b4a22a45c026f053712e`  
		Last Modified: Mon, 03 Jan 2022 21:48:32 GMT  
		Size: 2.4 MB (2441852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718568f6bd9465712d09a6a588ca280d05d6b2e04d8f00bd708505e5ba89b673`  
		Last Modified: Mon, 03 Jan 2022 21:48:32 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f651239b468779a655f7ba10cd4061935be60a0f115e5a33161da7835651a1`  
		Last Modified: Mon, 03 Jan 2022 22:25:59 GMT  
		Size: 10.1 MB (10092953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed549551cbe4f7a01323358af11c6c600d947f1ad22809e122efe93b8c76e3`  
		Last Modified: Mon, 03 Jan 2022 22:25:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `express-gateway:1.16.x`

```console
$ docker pull express-gateway@sha256:301a745e5c9156164ff3b56fd6a4abca1ae4fd1f6ef90912707d93db9881702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:1.16.x` - linux; amd64

```console
$ docker pull express-gateway@sha256:b2c2c32f328db5774e533d775cfee3a168392eb5a1ac8956a2fc4d928fa9e1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40215767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4750d89b8c24f3fec3de71ea88a938aa0a96344bfa99c27ceb3bc2562e9193b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 21:23:29 GMT
ENV NODE_VERSION=12.22.9
# Tue, 11 Jan 2022 21:23:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bda831fbebfc00d12dbbc59b6d3736350d8cfbd495753c725800db10e591eb20"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 21:23:41 GMT
ENV YARN_VERSION=1.22.17
# Wed, 12 Jan 2022 00:13:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 12 Jan 2022 00:13:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:13:25 GMT
CMD ["node"]
# Wed, 12 Jan 2022 00:21:07 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 12 Jan 2022 00:21:07 GMT
ARG EG_VERSION=1.16.11
# Wed, 12 Jan 2022 00:21:40 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 12 Jan 2022 00:21:40 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 00:21:40 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 12 Jan 2022 00:21:41 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 12 Jan 2022 00:21:41 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 12 Jan 2022 00:21:41 GMT
VOLUME [/var/lib/eg]
# Wed, 12 Jan 2022 00:21:41 GMT
EXPOSE 8080 9876
# Wed, 12 Jan 2022 00:21:41 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:21:42 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea1bcfc51681a204ae05c69001c5b7d72bf091d2bfa06f18db72f380ab7494`  
		Last Modified: Wed, 12 Jan 2022 00:18:22 GMT  
		Size: 24.9 MB (24935078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55284a5c72ce1ed6a1c6a6601d67bdabdb0fa7d111921adca44238fdb08c71af`  
		Last Modified: Wed, 12 Jan 2022 00:18:16 GMT  
		Size: 2.4 MB (2367619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9867c49b9ebe6a7af9f0066c7b4fbdd083d658335b83c57c57f368abb43de92`  
		Last Modified: Wed, 12 Jan 2022 00:18:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fed4adb9d69e261ebc708fd9d3eb2892d6d2438d06a99494b7118a03d4c8612`  
		Last Modified: Wed, 12 Jan 2022 00:22:02 GMT  
		Size: 10.1 MB (10093701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b0b1eb8db440077d2b3cd8ffb7687dacf0819c76c05390c41e81d3aa231c88`  
		Last Modified: Wed, 12 Jan 2022 00:21:59 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:761cea51c7d1d098a65ed31ff9f9502c93bdd23aa9f17214c6ba6fab6967e74a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40076361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e095f6879a7f80a5fd4ebc9e9967a58fbb00a32a2057538cc506678b0b70a81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 22:48:50 GMT
ENV NODE_VERSION=12.22.9
# Tue, 11 Jan 2022 23:06:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bda831fbebfc00d12dbbc59b6d3736350d8cfbd495753c725800db10e591eb20"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 23:06:18 GMT
ENV YARN_VERSION=1.22.17
# Tue, 11 Jan 2022 23:06:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 11 Jan 2022 23:06:25 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 11 Jan 2022 23:06:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jan 2022 23:06:26 GMT
CMD ["node"]
# Wed, 12 Jan 2022 00:36:26 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 12 Jan 2022 00:36:26 GMT
ARG EG_VERSION=1.16.11
# Wed, 12 Jan 2022 00:36:46 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 12 Jan 2022 00:36:47 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 00:36:48 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 12 Jan 2022 00:36:48 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 12 Jan 2022 00:36:49 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 12 Jan 2022 00:36:50 GMT
VOLUME [/var/lib/eg]
# Wed, 12 Jan 2022 00:36:51 GMT
EXPOSE 8080 9876
# Wed, 12 Jan 2022 00:36:53 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:36:54 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9060f367f1180782ca5f4ea561eb558b819462f985f2668562d1b3aa8b46bfdb`  
		Last Modified: Tue, 11 Jan 2022 23:29:32 GMT  
		Size: 24.8 MB (24821785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f579526409f0efbcc848745755ec3dbc748f6e855037f1e709f1d9cdadea5e62`  
		Last Modified: Tue, 11 Jan 2022 23:29:28 GMT  
		Size: 2.4 MB (2439307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2bc6a98cc8a0b0bd450c2c88a6db2f26a9810c044ea9c66acef24ae05a6adf`  
		Last Modified: Tue, 11 Jan 2022 23:29:27 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbf831da352b388d9efa20075d78154468310e5d3763a99fa983ea15c4574e`  
		Last Modified: Wed, 12 Jan 2022 00:37:18 GMT  
		Size: 10.1 MB (10098887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126af8567de32913438641b026f7c72c90ec372b688bbe02a1cbdbb578f4dff1`  
		Last Modified: Wed, 12 Jan 2022 00:37:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:7b8658ac6172e70175d37d3a35dfcc58d0a1478ff8944f0289deb39955720e80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42500616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ccea382dda64286cf1e6442b00317514697f4fe10347fe29f0262a9cd2eaf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Mon, 03 Jan 2022 20:52:20 GMT
ENV NODE_VERSION=12.22.8
# Mon, 03 Jan 2022 21:10:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="9cc1d120c404d66a62d6e4daaba361e8e1996bdc5b9643f97bbd1241247332df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 03 Jan 2022 21:11:02 GMT
ENV YARN_VERSION=1.22.17
# Mon, 03 Jan 2022 21:11:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 03 Jan 2022 21:11:14 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 03 Jan 2022 21:11:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 21:11:17 GMT
CMD ["node"]
# Mon, 03 Jan 2022 22:31:44 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Mon, 03 Jan 2022 22:31:47 GMT
ARG EG_VERSION=1.16.11
# Mon, 03 Jan 2022 22:32:25 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Mon, 03 Jan 2022 22:32:31 GMT
ENV NODE_ENV=production
# Mon, 03 Jan 2022 22:32:34 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Mon, 03 Jan 2022 22:32:36 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Mon, 03 Jan 2022 22:32:38 GMT
ENV CHOKIDAR_USEPOLLING=true
# Mon, 03 Jan 2022 22:32:42 GMT
VOLUME [/var/lib/eg]
# Mon, 03 Jan 2022 22:32:44 GMT
EXPOSE 8080 9876
# Mon, 03 Jan 2022 22:32:45 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Mon, 03 Jan 2022 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 22:32:50 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd8ae3ce34c1b7eb183bbf0256c324cca8320fbd95714db3073e3c87a025d4`  
		Last Modified: Mon, 03 Jan 2022 21:19:22 GMT  
		Size: 27.2 MB (27152474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb88dcbb6546833e6ff1d90decf1ca584f3d1222966bb3622d8ef26cc30240a`  
		Last Modified: Mon, 03 Jan 2022 21:19:17 GMT  
		Size: 2.4 MB (2439494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e241b4784ab1e6ed8e73c40e765eb635694f16ebb8eb56a5c3a31b8d0c698a89`  
		Last Modified: Mon, 03 Jan 2022 21:19:16 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d143ea5e0b7ab4240374827d452cc0c552e1475922c72ba363e88bbd77ba1c1a`  
		Last Modified: Mon, 03 Jan 2022 22:33:23 GMT  
		Size: 10.1 MB (10092925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fcdf040429b2c88cc60a69a745aea3c425255262d281380ef480bf2546ce`  
		Last Modified: Mon, 03 Jan 2022 22:33:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.16.x` - linux; s390x

```console
$ docker pull express-gateway@sha256:65ef90c1b4769878961cf3120838bd1a4d172a71c80c7f5cfc55fa445e04494c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39964175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a081214b069709185112015b57d8132bc30db8f911b27c1ac66dd4bc64213bd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Mon, 03 Jan 2022 21:20:28 GMT
ENV NODE_VERSION=12.22.8
# Mon, 03 Jan 2022 21:40:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="9cc1d120c404d66a62d6e4daaba361e8e1996bdc5b9643f97bbd1241247332df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 03 Jan 2022 21:40:59 GMT
ENV YARN_VERSION=1.22.17
# Mon, 03 Jan 2022 21:41:03 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 03 Jan 2022 21:41:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 03 Jan 2022 21:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 21:41:04 GMT
CMD ["node"]
# Mon, 03 Jan 2022 22:25:10 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Mon, 03 Jan 2022 22:25:10 GMT
ARG EG_VERSION=1.16.11
# Mon, 03 Jan 2022 22:25:33 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Mon, 03 Jan 2022 22:25:36 GMT
ENV NODE_ENV=production
# Mon, 03 Jan 2022 22:25:36 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Mon, 03 Jan 2022 22:25:37 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Mon, 03 Jan 2022 22:25:37 GMT
ENV CHOKIDAR_USEPOLLING=true
# Mon, 03 Jan 2022 22:25:37 GMT
VOLUME [/var/lib/eg]
# Mon, 03 Jan 2022 22:25:37 GMT
EXPOSE 8080 9876
# Mon, 03 Jan 2022 22:25:37 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Mon, 03 Jan 2022 22:25:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 22:25:38 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17afc4c4e622a9d3ffec3b18b57875679992dd76ad7da3cd328b8c835477fd0`  
		Last Modified: Mon, 03 Jan 2022 21:48:36 GMT  
		Size: 24.8 MB (24822482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901c31be32d2518467b683d91a3707b8d1aa1a692ce2b4a22a45c026f053712e`  
		Last Modified: Mon, 03 Jan 2022 21:48:32 GMT  
		Size: 2.4 MB (2441852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718568f6bd9465712d09a6a588ca280d05d6b2e04d8f00bd708505e5ba89b673`  
		Last Modified: Mon, 03 Jan 2022 21:48:32 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f651239b468779a655f7ba10cd4061935be60a0f115e5a33161da7835651a1`  
		Last Modified: Mon, 03 Jan 2022 22:25:59 GMT  
		Size: 10.1 MB (10092953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed549551cbe4f7a01323358af11c6c600d947f1ad22809e122efe93b8c76e3`  
		Last Modified: Mon, 03 Jan 2022 22:25:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `express-gateway:1.x`

```console
$ docker pull express-gateway@sha256:301a745e5c9156164ff3b56fd6a4abca1ae4fd1f6ef90912707d93db9881702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:1.x` - linux; amd64

```console
$ docker pull express-gateway@sha256:b2c2c32f328db5774e533d775cfee3a168392eb5a1ac8956a2fc4d928fa9e1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40215767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4750d89b8c24f3fec3de71ea88a938aa0a96344bfa99c27ceb3bc2562e9193b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 21:23:29 GMT
ENV NODE_VERSION=12.22.9
# Tue, 11 Jan 2022 21:23:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bda831fbebfc00d12dbbc59b6d3736350d8cfbd495753c725800db10e591eb20"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 21:23:41 GMT
ENV YARN_VERSION=1.22.17
# Wed, 12 Jan 2022 00:13:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 12 Jan 2022 00:13:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:13:25 GMT
CMD ["node"]
# Wed, 12 Jan 2022 00:21:07 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 12 Jan 2022 00:21:07 GMT
ARG EG_VERSION=1.16.11
# Wed, 12 Jan 2022 00:21:40 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 12 Jan 2022 00:21:40 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 00:21:40 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 12 Jan 2022 00:21:41 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 12 Jan 2022 00:21:41 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 12 Jan 2022 00:21:41 GMT
VOLUME [/var/lib/eg]
# Wed, 12 Jan 2022 00:21:41 GMT
EXPOSE 8080 9876
# Wed, 12 Jan 2022 00:21:41 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:21:42 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea1bcfc51681a204ae05c69001c5b7d72bf091d2bfa06f18db72f380ab7494`  
		Last Modified: Wed, 12 Jan 2022 00:18:22 GMT  
		Size: 24.9 MB (24935078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55284a5c72ce1ed6a1c6a6601d67bdabdb0fa7d111921adca44238fdb08c71af`  
		Last Modified: Wed, 12 Jan 2022 00:18:16 GMT  
		Size: 2.4 MB (2367619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9867c49b9ebe6a7af9f0066c7b4fbdd083d658335b83c57c57f368abb43de92`  
		Last Modified: Wed, 12 Jan 2022 00:18:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fed4adb9d69e261ebc708fd9d3eb2892d6d2438d06a99494b7118a03d4c8612`  
		Last Modified: Wed, 12 Jan 2022 00:22:02 GMT  
		Size: 10.1 MB (10093701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b0b1eb8db440077d2b3cd8ffb7687dacf0819c76c05390c41e81d3aa231c88`  
		Last Modified: Wed, 12 Jan 2022 00:21:59 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:761cea51c7d1d098a65ed31ff9f9502c93bdd23aa9f17214c6ba6fab6967e74a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40076361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e095f6879a7f80a5fd4ebc9e9967a58fbb00a32a2057538cc506678b0b70a81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 22:48:50 GMT
ENV NODE_VERSION=12.22.9
# Tue, 11 Jan 2022 23:06:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bda831fbebfc00d12dbbc59b6d3736350d8cfbd495753c725800db10e591eb20"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 23:06:18 GMT
ENV YARN_VERSION=1.22.17
# Tue, 11 Jan 2022 23:06:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 11 Jan 2022 23:06:25 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 11 Jan 2022 23:06:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jan 2022 23:06:26 GMT
CMD ["node"]
# Wed, 12 Jan 2022 00:36:26 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 12 Jan 2022 00:36:26 GMT
ARG EG_VERSION=1.16.11
# Wed, 12 Jan 2022 00:36:46 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 12 Jan 2022 00:36:47 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 00:36:48 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 12 Jan 2022 00:36:48 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 12 Jan 2022 00:36:49 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 12 Jan 2022 00:36:50 GMT
VOLUME [/var/lib/eg]
# Wed, 12 Jan 2022 00:36:51 GMT
EXPOSE 8080 9876
# Wed, 12 Jan 2022 00:36:53 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:36:54 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9060f367f1180782ca5f4ea561eb558b819462f985f2668562d1b3aa8b46bfdb`  
		Last Modified: Tue, 11 Jan 2022 23:29:32 GMT  
		Size: 24.8 MB (24821785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f579526409f0efbcc848745755ec3dbc748f6e855037f1e709f1d9cdadea5e62`  
		Last Modified: Tue, 11 Jan 2022 23:29:28 GMT  
		Size: 2.4 MB (2439307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2bc6a98cc8a0b0bd450c2c88a6db2f26a9810c044ea9c66acef24ae05a6adf`  
		Last Modified: Tue, 11 Jan 2022 23:29:27 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbf831da352b388d9efa20075d78154468310e5d3763a99fa983ea15c4574e`  
		Last Modified: Wed, 12 Jan 2022 00:37:18 GMT  
		Size: 10.1 MB (10098887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126af8567de32913438641b026f7c72c90ec372b688bbe02a1cbdbb578f4dff1`  
		Last Modified: Wed, 12 Jan 2022 00:37:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:7b8658ac6172e70175d37d3a35dfcc58d0a1478ff8944f0289deb39955720e80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42500616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ccea382dda64286cf1e6442b00317514697f4fe10347fe29f0262a9cd2eaf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Mon, 03 Jan 2022 20:52:20 GMT
ENV NODE_VERSION=12.22.8
# Mon, 03 Jan 2022 21:10:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="9cc1d120c404d66a62d6e4daaba361e8e1996bdc5b9643f97bbd1241247332df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 03 Jan 2022 21:11:02 GMT
ENV YARN_VERSION=1.22.17
# Mon, 03 Jan 2022 21:11:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 03 Jan 2022 21:11:14 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 03 Jan 2022 21:11:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 21:11:17 GMT
CMD ["node"]
# Mon, 03 Jan 2022 22:31:44 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Mon, 03 Jan 2022 22:31:47 GMT
ARG EG_VERSION=1.16.11
# Mon, 03 Jan 2022 22:32:25 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Mon, 03 Jan 2022 22:32:31 GMT
ENV NODE_ENV=production
# Mon, 03 Jan 2022 22:32:34 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Mon, 03 Jan 2022 22:32:36 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Mon, 03 Jan 2022 22:32:38 GMT
ENV CHOKIDAR_USEPOLLING=true
# Mon, 03 Jan 2022 22:32:42 GMT
VOLUME [/var/lib/eg]
# Mon, 03 Jan 2022 22:32:44 GMT
EXPOSE 8080 9876
# Mon, 03 Jan 2022 22:32:45 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Mon, 03 Jan 2022 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 22:32:50 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd8ae3ce34c1b7eb183bbf0256c324cca8320fbd95714db3073e3c87a025d4`  
		Last Modified: Mon, 03 Jan 2022 21:19:22 GMT  
		Size: 27.2 MB (27152474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb88dcbb6546833e6ff1d90decf1ca584f3d1222966bb3622d8ef26cc30240a`  
		Last Modified: Mon, 03 Jan 2022 21:19:17 GMT  
		Size: 2.4 MB (2439494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e241b4784ab1e6ed8e73c40e765eb635694f16ebb8eb56a5c3a31b8d0c698a89`  
		Last Modified: Mon, 03 Jan 2022 21:19:16 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d143ea5e0b7ab4240374827d452cc0c552e1475922c72ba363e88bbd77ba1c1a`  
		Last Modified: Mon, 03 Jan 2022 22:33:23 GMT  
		Size: 10.1 MB (10092925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fcdf040429b2c88cc60a69a745aea3c425255262d281380ef480bf2546ce`  
		Last Modified: Mon, 03 Jan 2022 22:33:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:1.x` - linux; s390x

```console
$ docker pull express-gateway@sha256:65ef90c1b4769878961cf3120838bd1a4d172a71c80c7f5cfc55fa445e04494c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39964175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a081214b069709185112015b57d8132bc30db8f911b27c1ac66dd4bc64213bd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Mon, 03 Jan 2022 21:20:28 GMT
ENV NODE_VERSION=12.22.8
# Mon, 03 Jan 2022 21:40:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="9cc1d120c404d66a62d6e4daaba361e8e1996bdc5b9643f97bbd1241247332df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 03 Jan 2022 21:40:59 GMT
ENV YARN_VERSION=1.22.17
# Mon, 03 Jan 2022 21:41:03 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 03 Jan 2022 21:41:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 03 Jan 2022 21:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 21:41:04 GMT
CMD ["node"]
# Mon, 03 Jan 2022 22:25:10 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Mon, 03 Jan 2022 22:25:10 GMT
ARG EG_VERSION=1.16.11
# Mon, 03 Jan 2022 22:25:33 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Mon, 03 Jan 2022 22:25:36 GMT
ENV NODE_ENV=production
# Mon, 03 Jan 2022 22:25:36 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Mon, 03 Jan 2022 22:25:37 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Mon, 03 Jan 2022 22:25:37 GMT
ENV CHOKIDAR_USEPOLLING=true
# Mon, 03 Jan 2022 22:25:37 GMT
VOLUME [/var/lib/eg]
# Mon, 03 Jan 2022 22:25:37 GMT
EXPOSE 8080 9876
# Mon, 03 Jan 2022 22:25:37 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Mon, 03 Jan 2022 22:25:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 22:25:38 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17afc4c4e622a9d3ffec3b18b57875679992dd76ad7da3cd328b8c835477fd0`  
		Last Modified: Mon, 03 Jan 2022 21:48:36 GMT  
		Size: 24.8 MB (24822482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901c31be32d2518467b683d91a3707b8d1aa1a692ce2b4a22a45c026f053712e`  
		Last Modified: Mon, 03 Jan 2022 21:48:32 GMT  
		Size: 2.4 MB (2441852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718568f6bd9465712d09a6a588ca280d05d6b2e04d8f00bd708505e5ba89b673`  
		Last Modified: Mon, 03 Jan 2022 21:48:32 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f651239b468779a655f7ba10cd4061935be60a0f115e5a33161da7835651a1`  
		Last Modified: Mon, 03 Jan 2022 22:25:59 GMT  
		Size: 10.1 MB (10092953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed549551cbe4f7a01323358af11c6c600d947f1ad22809e122efe93b8c76e3`  
		Last Modified: Mon, 03 Jan 2022 22:25:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `express-gateway:latest`

```console
$ docker pull express-gateway@sha256:301a745e5c9156164ff3b56fd6a4abca1ae4fd1f6ef90912707d93db9881702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `express-gateway:latest` - linux; amd64

```console
$ docker pull express-gateway@sha256:b2c2c32f328db5774e533d775cfee3a168392eb5a1ac8956a2fc4d928fa9e1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40215767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4750d89b8c24f3fec3de71ea88a938aa0a96344bfa99c27ceb3bc2562e9193b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 21:23:29 GMT
ENV NODE_VERSION=12.22.9
# Tue, 11 Jan 2022 21:23:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bda831fbebfc00d12dbbc59b6d3736350d8cfbd495753c725800db10e591eb20"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 21:23:41 GMT
ENV YARN_VERSION=1.22.17
# Wed, 12 Jan 2022 00:13:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 12 Jan 2022 00:13:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:13:25 GMT
CMD ["node"]
# Wed, 12 Jan 2022 00:21:07 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 12 Jan 2022 00:21:07 GMT
ARG EG_VERSION=1.16.11
# Wed, 12 Jan 2022 00:21:40 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 12 Jan 2022 00:21:40 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 00:21:40 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 12 Jan 2022 00:21:41 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 12 Jan 2022 00:21:41 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 12 Jan 2022 00:21:41 GMT
VOLUME [/var/lib/eg]
# Wed, 12 Jan 2022 00:21:41 GMT
EXPOSE 8080 9876
# Wed, 12 Jan 2022 00:21:41 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:21:42 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea1bcfc51681a204ae05c69001c5b7d72bf091d2bfa06f18db72f380ab7494`  
		Last Modified: Wed, 12 Jan 2022 00:18:22 GMT  
		Size: 24.9 MB (24935078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55284a5c72ce1ed6a1c6a6601d67bdabdb0fa7d111921adca44238fdb08c71af`  
		Last Modified: Wed, 12 Jan 2022 00:18:16 GMT  
		Size: 2.4 MB (2367619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9867c49b9ebe6a7af9f0066c7b4fbdd083d658335b83c57c57f368abb43de92`  
		Last Modified: Wed, 12 Jan 2022 00:18:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fed4adb9d69e261ebc708fd9d3eb2892d6d2438d06a99494b7118a03d4c8612`  
		Last Modified: Wed, 12 Jan 2022 00:22:02 GMT  
		Size: 10.1 MB (10093701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b0b1eb8db440077d2b3cd8ffb7687dacf0819c76c05390c41e81d3aa231c88`  
		Last Modified: Wed, 12 Jan 2022 00:21:59 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; arm64 variant v8

```console
$ docker pull express-gateway@sha256:761cea51c7d1d098a65ed31ff9f9502c93bdd23aa9f17214c6ba6fab6967e74a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40076361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e095f6879a7f80a5fd4ebc9e9967a58fbb00a32a2057538cc506678b0b70a81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Jan 2022 22:48:50 GMT
ENV NODE_VERSION=12.22.9
# Tue, 11 Jan 2022 23:06:17 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="bda831fbebfc00d12dbbc59b6d3736350d8cfbd495753c725800db10e591eb20"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 11 Jan 2022 23:06:18 GMT
ENV YARN_VERSION=1.22.17
# Tue, 11 Jan 2022 23:06:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 11 Jan 2022 23:06:25 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 11 Jan 2022 23:06:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jan 2022 23:06:26 GMT
CMD ["node"]
# Wed, 12 Jan 2022 00:36:26 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Wed, 12 Jan 2022 00:36:26 GMT
ARG EG_VERSION=1.16.11
# Wed, 12 Jan 2022 00:36:46 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Wed, 12 Jan 2022 00:36:47 GMT
ENV NODE_ENV=production
# Wed, 12 Jan 2022 00:36:48 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Wed, 12 Jan 2022 00:36:48 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Wed, 12 Jan 2022 00:36:49 GMT
ENV CHOKIDAR_USEPOLLING=true
# Wed, 12 Jan 2022 00:36:50 GMT
VOLUME [/var/lib/eg]
# Wed, 12 Jan 2022 00:36:51 GMT
EXPOSE 8080 9876
# Wed, 12 Jan 2022 00:36:53 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Wed, 12 Jan 2022 00:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jan 2022 00:36:54 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9060f367f1180782ca5f4ea561eb558b819462f985f2668562d1b3aa8b46bfdb`  
		Last Modified: Tue, 11 Jan 2022 23:29:32 GMT  
		Size: 24.8 MB (24821785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f579526409f0efbcc848745755ec3dbc748f6e855037f1e709f1d9cdadea5e62`  
		Last Modified: Tue, 11 Jan 2022 23:29:28 GMT  
		Size: 2.4 MB (2439307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2bc6a98cc8a0b0bd450c2c88a6db2f26a9810c044ea9c66acef24ae05a6adf`  
		Last Modified: Tue, 11 Jan 2022 23:29:27 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbf831da352b388d9efa20075d78154468310e5d3763a99fa983ea15c4574e`  
		Last Modified: Wed, 12 Jan 2022 00:37:18 GMT  
		Size: 10.1 MB (10098887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126af8567de32913438641b026f7c72c90ec372b688bbe02a1cbdbb578f4dff1`  
		Last Modified: Wed, 12 Jan 2022 00:37:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; ppc64le

```console
$ docker pull express-gateway@sha256:7b8658ac6172e70175d37d3a35dfcc58d0a1478ff8944f0289deb39955720e80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42500616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ccea382dda64286cf1e6442b00317514697f4fe10347fe29f0262a9cd2eaf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Mon, 03 Jan 2022 20:52:20 GMT
ENV NODE_VERSION=12.22.8
# Mon, 03 Jan 2022 21:10:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="9cc1d120c404d66a62d6e4daaba361e8e1996bdc5b9643f97bbd1241247332df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 03 Jan 2022 21:11:02 GMT
ENV YARN_VERSION=1.22.17
# Mon, 03 Jan 2022 21:11:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 03 Jan 2022 21:11:14 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 03 Jan 2022 21:11:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 21:11:17 GMT
CMD ["node"]
# Mon, 03 Jan 2022 22:31:44 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Mon, 03 Jan 2022 22:31:47 GMT
ARG EG_VERSION=1.16.11
# Mon, 03 Jan 2022 22:32:25 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Mon, 03 Jan 2022 22:32:31 GMT
ENV NODE_ENV=production
# Mon, 03 Jan 2022 22:32:34 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Mon, 03 Jan 2022 22:32:36 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Mon, 03 Jan 2022 22:32:38 GMT
ENV CHOKIDAR_USEPOLLING=true
# Mon, 03 Jan 2022 22:32:42 GMT
VOLUME [/var/lib/eg]
# Mon, 03 Jan 2022 22:32:44 GMT
EXPOSE 8080 9876
# Mon, 03 Jan 2022 22:32:45 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Mon, 03 Jan 2022 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 22:32:50 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd8ae3ce34c1b7eb183bbf0256c324cca8320fbd95714db3073e3c87a025d4`  
		Last Modified: Mon, 03 Jan 2022 21:19:22 GMT  
		Size: 27.2 MB (27152474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb88dcbb6546833e6ff1d90decf1ca584f3d1222966bb3622d8ef26cc30240a`  
		Last Modified: Mon, 03 Jan 2022 21:19:17 GMT  
		Size: 2.4 MB (2439494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e241b4784ab1e6ed8e73c40e765eb635694f16ebb8eb56a5c3a31b8d0c698a89`  
		Last Modified: Mon, 03 Jan 2022 21:19:16 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d143ea5e0b7ab4240374827d452cc0c552e1475922c72ba363e88bbd77ba1c1a`  
		Last Modified: Mon, 03 Jan 2022 22:33:23 GMT  
		Size: 10.1 MB (10092925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fcdf040429b2c88cc60a69a745aea3c425255262d281380ef480bf2546ce`  
		Last Modified: Mon, 03 Jan 2022 22:33:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `express-gateway:latest` - linux; s390x

```console
$ docker pull express-gateway@sha256:65ef90c1b4769878961cf3120838bd1a4d172a71c80c7f5cfc55fa445e04494c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39964175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a081214b069709185112015b57d8132bc30db8f911b27c1ac66dd4bc64213bd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","-e","require('express-gateway')().run();"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Mon, 03 Jan 2022 21:20:28 GMT
ENV NODE_VERSION=12.22.8
# Mon, 03 Jan 2022 21:40:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="9cc1d120c404d66a62d6e4daaba361e8e1996bdc5b9643f97bbd1241247332df"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 03 Jan 2022 21:40:59 GMT
ENV YARN_VERSION=1.22.17
# Mon, 03 Jan 2022 21:41:03 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 03 Jan 2022 21:41:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 03 Jan 2022 21:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 21:41:04 GMT
CMD ["node"]
# Mon, 03 Jan 2022 22:25:10 GMT
LABEL maintainer=Vincenzo Chianese, vincenzo@express-gateway.io
# Mon, 03 Jan 2022 22:25:10 GMT
ARG EG_VERSION=1.16.11
# Mon, 03 Jan 2022 22:25:33 GMT
# ARGS: EG_VERSION=1.16.11
RUN yarn global add express-gateway@$EG_VERSION && yarn cache clean
# Mon, 03 Jan 2022 22:25:36 GMT
ENV NODE_ENV=production
# Mon, 03 Jan 2022 22:25:36 GMT
ENV NODE_PATH=/usr/local/share/.config/yarn/global/node_modules/
# Mon, 03 Jan 2022 22:25:37 GMT
ENV EG_CONFIG_DIR=/var/lib/eg
# Mon, 03 Jan 2022 22:25:37 GMT
ENV CHOKIDAR_USEPOLLING=true
# Mon, 03 Jan 2022 22:25:37 GMT
VOLUME [/var/lib/eg]
# Mon, 03 Jan 2022 22:25:37 GMT
EXPOSE 8080 9876
# Mon, 03 Jan 2022 22:25:37 GMT
COPY file:9481e65ab3ccc3b910b8af90d3df04d9f70030b8f8a0cfcc390840936290aaab in /usr/local/bin/ 
# Mon, 03 Jan 2022 22:25:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jan 2022 22:25:38 GMT
CMD ["node" "-e" "require('express-gateway')().run();"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17afc4c4e622a9d3ffec3b18b57875679992dd76ad7da3cd328b8c835477fd0`  
		Last Modified: Mon, 03 Jan 2022 21:48:36 GMT  
		Size: 24.8 MB (24822482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901c31be32d2518467b683d91a3707b8d1aa1a692ce2b4a22a45c026f053712e`  
		Last Modified: Mon, 03 Jan 2022 21:48:32 GMT  
		Size: 2.4 MB (2441852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718568f6bd9465712d09a6a588ca280d05d6b2e04d8f00bd708505e5ba89b673`  
		Last Modified: Mon, 03 Jan 2022 21:48:32 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f651239b468779a655f7ba10cd4061935be60a0f115e5a33161da7835651a1`  
		Last Modified: Mon, 03 Jan 2022 22:25:59 GMT  
		Size: 10.1 MB (10092953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed549551cbe4f7a01323358af11c6c600d947f1ad22809e122efe93b8c76e3`  
		Last Modified: Mon, 03 Jan 2022 22:25:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
