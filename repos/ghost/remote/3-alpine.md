## `ghost:3-alpine`

```console
$ docker pull ghost@sha256:17e8b725a63a28521338186028a5d12bc1fe298b04f03e7369ba1a704007af9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:3-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:dd754f68201f7c44f135aab10e40f82e6e2359a208945864a4f6e5e50a68c56a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110923657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43222d64b698afb51ddb08d2b1d5ea102d2cae9f6cab137c49458136e1fe6c65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 23:43:38 GMT
ENV NODE_VERSION=12.22.6
# Tue, 31 Aug 2021 23:43:44 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0ce2b97ecbbd84f1a5ed13278ed6845d93c6454d8550730b247a990438dba322"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 31 Aug 2021 23:43:45 GMT
ENV YARN_VERSION=1.22.5
# Tue, 31 Aug 2021 23:43:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 31 Aug 2021 23:43:50 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 31 Aug 2021 23:43:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Aug 2021 23:43:50 GMT
CMD ["node"]
# Wed, 01 Sep 2021 00:02:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 00:02:54 GMT
RUN apk add --no-cache 		bash
# Wed, 01 Sep 2021 00:02:55 GMT
ENV NODE_ENV=production
# Wed, 01 Sep 2021 00:02:55 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Wed, 01 Sep 2021 00:03:29 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 01 Sep 2021 00:03:31 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 01 Sep 2021 00:03:31 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 01 Sep 2021 00:03:31 GMT
ENV GHOST_VERSION=3.42.5
# Wed, 01 Sep 2021 00:05:31 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 01 Sep 2021 00:05:34 GMT
WORKDIR /var/lib/ghost
# Wed, 01 Sep 2021 00:05:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 01 Sep 2021 00:05:35 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Wed, 01 Sep 2021 00:05:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:05:36 GMT
EXPOSE 2368
# Wed, 01 Sep 2021 00:05:36 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b5709388fa3362bce7644938eb39a202286180813eadada42c563250b3f368`  
		Last Modified: Tue, 31 Aug 2021 23:53:01 GMT  
		Size: 24.7 MB (24743091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e634a4e58d842de28619b45a9dfee6c4a225bf86ec06a5b20c6f221a8c1eafb7`  
		Last Modified: Tue, 31 Aug 2021 23:52:56 GMT  
		Size: 2.4 MB (2362329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcef3a4dbfe1a2419add12f62bf7f1182d29936031b2cc1cf274a6132cb01a8`  
		Last Modified: Tue, 31 Aug 2021 23:52:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d4c690ebdc7d0fc508bf7e134fafdf2bc7879ca480f9b1c551d874f5f0028e`  
		Last Modified: Wed, 01 Sep 2021 00:08:01 GMT  
		Size: 10.1 KB (10066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3794b24246d40d3cb18891a7081c706225b6b40caa0b44abd6476b033388b`  
		Last Modified: Wed, 01 Sep 2021 00:08:02 GMT  
		Size: 779.6 KB (779619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4b503e6a84b11b3546c3b00f91dacfa00ba6652446b354f3f6e711a9d29e39`  
		Last Modified: Wed, 01 Sep 2021 00:08:07 GMT  
		Size: 9.4 MB (9398357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7fe2d723b427fecf95ac23fb2c095dc1a16017119f3d18b8e2ba8fafd40970`  
		Last Modified: Wed, 01 Sep 2021 00:08:24 GMT  
		Size: 70.8 MB (70827659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a09bc7ec94456be7f2aaf4ad04ebb176111c1e9ef6dc35c318f9b90d072ab8f`  
		Last Modified: Wed, 01 Sep 2021 00:08:01 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:37b9ca141b540f56b588d701cb05b671adad1346386f89ff5fa7641318274e89
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94874206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c972737b471bfede8f1e3a6634490db581b9fbc4b1cb3ffd03c5e2795778a840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:45 GMT
ADD file:6b70601c3d32558ee0cefe87b44ce4c4c8e85db5211f940538f9acf03f6ba6be in / 
# Tue, 31 Aug 2021 22:30:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 04:39:31 GMT
ENV NODE_VERSION=12.22.6
# Wed, 01 Sep 2021 05:04:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0ce2b97ecbbd84f1a5ed13278ed6845d93c6454d8550730b247a990438dba322"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 01 Sep 2021 05:04:13 GMT
ENV YARN_VERSION=1.22.5
# Wed, 01 Sep 2021 05:04:23 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 01 Sep 2021 05:04:25 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 01 Sep 2021 05:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 05:04:26 GMT
CMD ["node"]
# Wed, 01 Sep 2021 08:49:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 08:49:55 GMT
RUN apk add --no-cache 		bash
# Wed, 01 Sep 2021 08:49:56 GMT
ENV NODE_ENV=production
# Wed, 01 Sep 2021 08:49:56 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Wed, 01 Sep 2021 08:51:18 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 01 Sep 2021 08:51:20 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 01 Sep 2021 08:51:20 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 01 Sep 2021 08:51:21 GMT
ENV GHOST_VERSION=3.42.5
# Wed, 01 Sep 2021 08:59:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 01 Sep 2021 09:00:00 GMT
WORKDIR /var/lib/ghost
# Wed, 01 Sep 2021 09:00:01 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 01 Sep 2021 09:00:01 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Wed, 01 Sep 2021 09:00:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 09:00:03 GMT
EXPOSE 2368
# Wed, 01 Sep 2021 09:00:03 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b3e69bfc382676dcc8e89f289815a72b60fdf61e66e21d90b8851cbb4b5e3aeb`  
		Last Modified: Tue, 31 Aug 2021 22:32:25 GMT  
		Size: 2.6 MB (2606586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0aa7b273235bdecb6e773aa7ab05583f910d870ee47ab600b5ca36274929c9`  
		Last Modified: Wed, 01 Sep 2021 05:39:24 GMT  
		Size: 24.2 MB (24171671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9a1c472fc76f442b961a7ff29a53767a7089090a7f00570dcc10140908e789`  
		Last Modified: Wed, 01 Sep 2021 05:39:06 GMT  
		Size: 2.4 MB (2414694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f6d2739dae8322273c2ccaaecae488388bf7ed5e41814b580ba7e893bcc4d0`  
		Last Modified: Wed, 01 Sep 2021 05:39:05 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4295a93b570e411365e0b3e02f1388e1fd6b95544ec1e2eda124eb20e276c3`  
		Last Modified: Wed, 01 Sep 2021 09:00:32 GMT  
		Size: 9.9 KB (9901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10778fc3ba7379ca9264b68ba525e986bf77e9bd6fa86e149aa9340b70c7e95a`  
		Last Modified: Wed, 01 Sep 2021 09:00:32 GMT  
		Size: 734.0 KB (734009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3f44af43cf7ccce750e39536e6099b099ed81a4e4fc0e8ce5cec4623f174a5`  
		Last Modified: Wed, 01 Sep 2021 09:00:46 GMT  
		Size: 9.4 MB (9399466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01c665044aabadc9ac2da1cd7a3a0ee9f2ea829dc9784c5a857795809a4e3b7`  
		Last Modified: Wed, 01 Sep 2021 09:01:46 GMT  
		Size: 55.5 MB (55537050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b886ecb8d20efa326ffa3904b7dc5b071f23b08528da3246459581e05290ebb`  
		Last Modified: Wed, 01 Sep 2021 09:00:32 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:7acecb756d2016ee1ef42dd2a9f2096f5346f37768f8ae593f3abb82a6132ce8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93669918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec5a0bc3954f2887f94e91944a83ef3faebefa006de92d0a25574db8b7b2a0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 01 Sep 2021 01:27:09 GMT
ADD file:fb3ea1e5df00e24345fc4f1adf07702f4ec457a6f7249f6ad06c72e2570955a0 in / 
# Wed, 01 Sep 2021 01:27:10 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:22:40 GMT
ENV NODE_VERSION=12.22.6
# Wed, 01 Sep 2021 06:36:14 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0ce2b97ecbbd84f1a5ed13278ed6845d93c6454d8550730b247a990438dba322"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 01 Sep 2021 06:36:15 GMT
ENV YARN_VERSION=1.22.5
# Wed, 01 Sep 2021 06:36:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 01 Sep 2021 06:36:23 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 01 Sep 2021 06:36:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 06:36:24 GMT
CMD ["node"]
# Wed, 01 Sep 2021 07:55:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 07:55:10 GMT
RUN apk add --no-cache 		bash
# Wed, 01 Sep 2021 07:55:11 GMT
ENV NODE_ENV=production
# Wed, 01 Sep 2021 07:55:11 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Wed, 01 Sep 2021 07:56:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 01 Sep 2021 07:56:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 01 Sep 2021 07:56:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 01 Sep 2021 07:56:17 GMT
ENV GHOST_VERSION=3.42.5
# Wed, 01 Sep 2021 08:02:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 01 Sep 2021 08:02:57 GMT
WORKDIR /var/lib/ghost
# Wed, 01 Sep 2021 08:02:58 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 01 Sep 2021 08:02:58 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Wed, 01 Sep 2021 08:02:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 08:02:59 GMT
EXPOSE 2368
# Wed, 01 Sep 2021 08:03:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b3b5e25c4f507c4fe7952504ebbc679023d8699d9c6b2b61376ed676d1ab572`  
		Last Modified: Wed, 01 Sep 2021 01:28:52 GMT  
		Size: 2.4 MB (2410387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402549befa7049277f1bdc2e3c51a391e084f6785fb60da4bcafdaa29a85922d`  
		Last Modified: Wed, 01 Sep 2021 07:16:14 GMT  
		Size: 23.7 MB (23728375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b603410b259d9586b8bb1f5a06f526cd8d8f29343105609986349921769c6a1f`  
		Last Modified: Wed, 01 Sep 2021 07:15:58 GMT  
		Size: 2.4 MB (2414631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0a9409eb77730dc6a61fc9f343f3e4056699781bfa32a4cc2a40a78ddf6859`  
		Last Modified: Wed, 01 Sep 2021 07:15:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8433f691e35b4165f0de86a0cfd1243fd35071c0b44015cbd6927683063bd0c4`  
		Last Modified: Wed, 01 Sep 2021 08:07:06 GMT  
		Size: 9.7 KB (9688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223f6ec13fff58e5409b0b4e9311141f28e333df98b4f3e351da1ec6ab5c8546`  
		Last Modified: Wed, 01 Sep 2021 08:07:07 GMT  
		Size: 671.2 KB (671151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc48898d75d372619fec3b88b9d5927e699a9e4283beff0809ba9f87e1a874b`  
		Last Modified: Wed, 01 Sep 2021 08:07:20 GMT  
		Size: 9.4 MB (9398413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f8c493422819a58e01975a9314c89b22a8634ab6284d1f93897028974bbeb0`  
		Last Modified: Wed, 01 Sep 2021 08:08:18 GMT  
		Size: 55.0 MB (55036448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970114ee9d7e190efecd6ea56504621e6348ae50efb3dcf3ab76a269202b3c59`  
		Last Modified: Wed, 01 Sep 2021 08:07:06 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d1c3802a0cbd8575ef93bb84c7c887f76ea939440e70d98ff1719534265bce8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95933532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5797c3dff1b0f85428f5ebeaf458aeb86c92b62b67f3a0205fdf996ffaf0bb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:52 GMT
ADD file:065608b23c19f03e2753bacf8f548d77f05519f94648c6872303aa1d1fc9254b in / 
# Wed, 01 Sep 2021 02:50:52 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 07:36:53 GMT
ENV NODE_VERSION=12.22.6
# Wed, 01 Sep 2021 08:04:36 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0ce2b97ecbbd84f1a5ed13278ed6845d93c6454d8550730b247a990438dba322"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 01 Sep 2021 08:04:36 GMT
ENV YARN_VERSION=1.22.5
# Wed, 01 Sep 2021 08:04:41 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 01 Sep 2021 08:04:41 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 01 Sep 2021 08:04:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 08:04:42 GMT
CMD ["node"]
# Wed, 01 Sep 2021 09:15:27 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 09:15:28 GMT
RUN apk add --no-cache 		bash
# Wed, 01 Sep 2021 09:15:28 GMT
ENV NODE_ENV=production
# Wed, 01 Sep 2021 09:15:29 GMT
ENV GHOST_CLI_VERSION=1.17.3
# Wed, 01 Sep 2021 09:15:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 01 Sep 2021 09:15:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 01 Sep 2021 09:15:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 01 Sep 2021 09:15:50 GMT
ENV GHOST_VERSION=3.42.5
# Wed, 01 Sep 2021 09:19:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Wed, 01 Sep 2021 09:19:09 GMT
WORKDIR /var/lib/ghost
# Wed, 01 Sep 2021 09:19:09 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 01 Sep 2021 09:19:09 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Wed, 01 Sep 2021 09:19:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 09:19:10 GMT
EXPOSE 2368
# Wed, 01 Sep 2021 09:19:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ccdebe76d52933c5fff4a8db8870e8454f3dc3c92a88e59acc5eb30c6c1178af`  
		Last Modified: Wed, 01 Sep 2021 02:51:48 GMT  
		Size: 2.7 MB (2712295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18439020eb7e8f88a0ae2492933c0bd11e8ffdcf030241eefa64e805093be410`  
		Last Modified: Wed, 01 Sep 2021 08:47:38 GMT  
		Size: 24.9 MB (24882613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3e027a943b1dc6fece375d65db556d52d64b8c88c2ef178b72487b2b20dac`  
		Last Modified: Wed, 01 Sep 2021 08:47:33 GMT  
		Size: 2.4 MB (2422767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c90772b68c8de6a07cd31be56632c2b8211db725f49210bae064249f17df24`  
		Last Modified: Wed, 01 Sep 2021 08:47:32 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c767c91524e4fee7743d45f532b6eed2d637d679e712b403ed7c696bcb9b9b`  
		Last Modified: Wed, 01 Sep 2021 09:20:53 GMT  
		Size: 10.0 KB (10011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b6beea65921e4cb8c008699c4bf98205a393b0dfb21aaa7da8c5d902648f41`  
		Last Modified: Wed, 01 Sep 2021 09:20:53 GMT  
		Size: 791.7 KB (791704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f942b5107b343422da90c8dace04718f0904350ebe2a9f43ea56e11f86579522`  
		Last Modified: Wed, 01 Sep 2021 09:20:56 GMT  
		Size: 9.4 MB (9398008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca90d45c33cd3cc26c59ad47eb902ff5329f8ef657e1cfef26c5282249110cae`  
		Last Modified: Wed, 01 Sep 2021 09:21:08 GMT  
		Size: 55.7 MB (55715306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f10b9de0b984cf5271d5ffb0212c27bf51583113eb359431223e1891911dbdd`  
		Last Modified: Wed, 01 Sep 2021 09:20:53 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
