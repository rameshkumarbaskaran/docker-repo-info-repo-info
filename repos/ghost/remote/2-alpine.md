## `ghost:2-alpine`

```console
$ docker pull ghost@sha256:6d589208c347e95ab5e78d780098b62133421ddd46052f8a30840788126868e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `ghost:2-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:d7bba4e94de31b4dea7e0f583041cecce303897817fb7c3ff08c817a1ec63f53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107627556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02045e34c7ded7666eb88ea79d2eff962b5d896ab6d5e1323bd8c0e55f42d0d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:21:07 GMT
ENV NODE_VERSION=10.24.1
# Wed, 14 Apr 2021 23:21:12 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 14 Apr 2021 23:21:13 GMT
ENV YARN_VERSION=1.22.5
# Wed, 14 Apr 2021 23:21:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 14 Apr 2021 23:21:16 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 14 Apr 2021 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:21:16 GMT
CMD ["node"]
# Thu, 15 Apr 2021 09:51:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 09:51:10 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 09:51:10 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 09:51:10 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 09:51:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 09:51:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 09:51:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Apr 2021 09:51:28 GMT
ENV GHOST_VERSION=2.38.3
# Thu, 15 Apr 2021 09:52:11 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 15 Apr 2021 09:52:12 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Apr 2021 09:52:13 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Apr 2021 09:52:13 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 15 Apr 2021 09:52:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 09:52:13 GMT
EXPOSE 2368
# Thu, 15 Apr 2021 09:52:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de915e575d22c7e33c83fddaf7aee0672e5d6a67e598a26fe0b30c7022f53cdd`  
		Last Modified: Wed, 14 Apr 2021 23:30:01 GMT  
		Size: 22.2 MB (22205881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7150aa69525b95f82b3df6a61a002f82382b2f3ea8ce51b9000b965f7476a5cc`  
		Last Modified: Wed, 14 Apr 2021 23:29:58 GMT  
		Size: 2.3 MB (2345009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7aa47be044e5a988e3e7f204e2e28cb9f070daa32ed081072ad6d5bf6c085d1`  
		Last Modified: Wed, 14 Apr 2021 23:29:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f070e3dcd2a1381f1e068a52190261d7ca9c3c5461e62cfac4b9de8fa8299896`  
		Last Modified: Thu, 15 Apr 2021 09:53:54 GMT  
		Size: 9.9 KB (9931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ee6fc3709b6400bd764cab71d6c2834450a526602aeed0ecd08f21b9effaa`  
		Last Modified: Thu, 15 Apr 2021 09:53:54 GMT  
		Size: 780.7 KB (780670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c347f775f0d40f3c5aa43d538d1d9f1cd024fa17b7123fbff640f67b781203`  
		Last Modified: Thu, 15 Apr 2021 09:53:56 GMT  
		Size: 7.4 MB (7404813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c6463556ba9265e5ac07fced7db52a4958ddc00a2b54d9ec0fe432f4b93a4a`  
		Last Modified: Thu, 15 Apr 2021 09:54:05 GMT  
		Size: 72.1 MB (72064178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213dae68808cfbadfc33e9027a09517cceb62826d3ddbf4045c11c14419cd336`  
		Last Modified: Thu, 15 Apr 2021 09:53:54 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:f7ad99ed46929c63d02b85b27b714c108751f2b9de4b9cd1af6287730e90fd92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92185791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d14d0ff029e710f0450c64b915dd013f268bc0b8162912d985e1bbd6728ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:58 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Wed, 14 Apr 2021 18:49:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:48:30 GMT
ENV NODE_VERSION=10.24.1
# Thu, 15 Apr 2021 00:57:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 00:57:26 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 00:57:34 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 00:57:35 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 00:57:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 00:57:37 GMT
CMD ["node"]
# Thu, 15 Apr 2021 07:01:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 07:01:08 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 07:01:09 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 07:01:10 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 07:01:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 07:01:58 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 07:01:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Apr 2021 07:02:00 GMT
ENV GHOST_VERSION=2.38.3
# Thu, 15 Apr 2021 07:07:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 15 Apr 2021 07:07:52 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Apr 2021 07:07:52 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Apr 2021 07:07:53 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 15 Apr 2021 07:07:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 07:07:55 GMT
EXPOSE 2368
# Thu, 15 Apr 2021 07:07:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543a0e4c5b199ecb0071f3ffd2e3d6836312f33e7fc43791deaeba9e07ee0b39`  
		Last Modified: Thu, 15 Apr 2021 01:06:00 GMT  
		Size: 21.6 MB (21647077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834b6f6f2970ebee2e7e405b0f3f9f75d9420c060e10974348f6999f68bbd0`  
		Last Modified: Thu, 15 Apr 2021 01:05:52 GMT  
		Size: 2.4 MB (2368285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099a180ab10c918a212d67a7ae4ebcb1eec8684047b4782225c1d622927e0aaf`  
		Last Modified: Thu, 15 Apr 2021 01:05:51 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8bdff355b0ed5484a2ac1ad32323817f55bba3e5aa63485fcbec8ebd71a28f`  
		Last Modified: Thu, 15 Apr 2021 07:09:54 GMT  
		Size: 9.7 KB (9740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49463e36a72b0c637ff7d6e22a0bf6efe657b1c960654d4006f10a4f0f38b5c0`  
		Last Modified: Thu, 15 Apr 2021 07:09:55 GMT  
		Size: 733.5 KB (733465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022cc7e447bb37eda7ef8249620cb3a34bfd261ac5a3077dc5c0f985ce08770`  
		Last Modified: Thu, 15 Apr 2021 07:10:00 GMT  
		Size: 7.4 MB (7405700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95676e3b67ea37f5033eff479a2872e387c13104c68daafe29eae8a1be3a63f`  
		Last Modified: Thu, 15 Apr 2021 07:10:23 GMT  
		Size: 57.4 MB (57398787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c6526e927f42176d8a6cc4acc051779cc1c784fce18b8c3147e3496d410c2`  
		Last Modified: Thu, 15 Apr 2021 07:09:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:53aaa4eee7080078e1fa1a224cfcf6ff566b08fbaecad722ea9b4f442ec2ed2d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91038617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ffcd809ad92b2723cf805996de7c6ba4cf4326ccccfcabb45544b0e8b7e084`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:58:03 GMT
ADD file:8aa5735295027f83674afe70bf82f93459836094a23f803762f0cbe410d459ac in / 
# Wed, 14 Apr 2021 18:58:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 01:52:08 GMT
ENV NODE_VERSION=10.24.1
# Thu, 15 Apr 2021 01:57:38 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 01:57:42 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 01:57:53 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 01:57:55 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 01:58:00 GMT
CMD ["node"]
# Thu, 15 Apr 2021 07:56:58 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 07:57:03 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 07:57:04 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 07:57:05 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 07:57:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 07:57:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 07:57:48 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Apr 2021 07:57:50 GMT
ENV GHOST_VERSION=2.38.3
# Thu, 15 Apr 2021 08:02:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 15 Apr 2021 08:02:20 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Apr 2021 08:02:21 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Apr 2021 08:02:22 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 15 Apr 2021 08:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:02:25 GMT
EXPOSE 2368
# Thu, 15 Apr 2021 08:02:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:07320de5da6bb708b6d53d6b2785c8d243d54a12708344df7b354fad9285ad3a`  
		Last Modified: Wed, 14 Apr 2021 18:58:55 GMT  
		Size: 2.4 MB (2424590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfc476b9f289f5f4ad81f84d1711a9a164693540adaf17e82e674dc62b1ed60`  
		Last Modified: Thu, 15 Apr 2021 02:06:44 GMT  
		Size: 21.2 MB (21246704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4886accda1683ed5e286e5d94c93394923c309c7a9c998aa20eea64d7d73546d`  
		Last Modified: Thu, 15 Apr 2021 02:06:33 GMT  
		Size: 2.4 MB (2368150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaaa7d5a2394f6ed878939062377fe952984ae3cabb53c1a583d98bb8f91c33`  
		Last Modified: Thu, 15 Apr 2021 02:06:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e532d050e8c5a4c4a55f98173ef5ff3051eff64c82960588fdd8d417f3016e00`  
		Last Modified: Thu, 15 Apr 2021 08:04:44 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d141941aae00b96d03ec4594ca319dfb7e5ff638b3a42662da54f18acf44947d`  
		Last Modified: Thu, 15 Apr 2021 08:04:44 GMT  
		Size: 669.0 KB (669038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e834412a18816dfd43df500c780141c11511a8e304891b6bafac9989f4760c21`  
		Last Modified: Thu, 15 Apr 2021 08:04:49 GMT  
		Size: 7.4 MB (7405633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a04bdd8c86c2eefe6debe1c1c15ba1083950003da0315bc95af8938fab88c5`  
		Last Modified: Thu, 15 Apr 2021 08:05:07 GMT  
		Size: 56.9 MB (56914150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e9336b29b2249d465d3c864016bb554470aa0d3f0b626d9638f74e9d5c46cd`  
		Last Modified: Thu, 15 Apr 2021 08:04:44 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:5e62e8600d77497d750d3039818d2e0447db1617236943f1725121b729983a26
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93339109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3789dd063c6bfe29fd8ce012fccd4d738f4143645acd2aeae0f9d138a8c70777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 04:12:22 GMT
ENV NODE_VERSION=10.24.1
# Thu, 15 Apr 2021 04:18:34 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 04:18:35 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 04:18:40 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 04:18:41 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 04:18:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 04:18:43 GMT
CMD ["node"]
# Thu, 15 Apr 2021 10:50:06 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 10:50:09 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 10:50:10 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 10:50:11 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 10:50:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 10:50:42 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 10:50:43 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Apr 2021 10:50:44 GMT
ENV GHOST_VERSION=2.38.3
# Thu, 15 Apr 2021 10:55:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 15 Apr 2021 10:55:16 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Apr 2021 10:55:17 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Apr 2021 10:55:18 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 15 Apr 2021 10:55:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 10:55:20 GMT
EXPOSE 2368
# Thu, 15 Apr 2021 10:55:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c43cfd44af11f89b8167480c786154d3f0d370606cd156da69ff0cf0956389`  
		Last Modified: Thu, 15 Apr 2021 04:28:15 GMT  
		Size: 22.5 MB (22464277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8393b5d5144cfccccc5ef02a524cdbcfd5c73975f3f24c3206a2722963a78de`  
		Last Modified: Thu, 15 Apr 2021 04:28:09 GMT  
		Size: 2.4 MB (2408223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ac3ba0a17ce3f95f099f3b2217dd8a31a0430647d5524ad0032b525cefeb70`  
		Last Modified: Thu, 15 Apr 2021 04:28:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecffa05d52730625beaeb8c3f87ea30d977c5e8c7a3a5648dd696f0edfcc3741`  
		Last Modified: Thu, 15 Apr 2021 10:57:09 GMT  
		Size: 9.9 KB (9855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5cfa69a6ae47f21ea7112355f930087dd300e3b3c9715a65fb52cf760c5d0c`  
		Last Modified: Thu, 15 Apr 2021 10:57:11 GMT  
		Size: 792.2 KB (792152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7def20b5485d04bc0a1faf928cf90eeedb7b014613f8c2ced0b43e081143760`  
		Last Modified: Thu, 15 Apr 2021 10:57:13 GMT  
		Size: 7.4 MB (7405370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bd7438819a7ded77d434871f1b307e5da2a7bdcbba50765f91f33083f6a8d`  
		Last Modified: Thu, 15 Apr 2021 10:57:32 GMT  
		Size: 57.5 MB (57531477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d8e7aa225d0d23339da0e164c6fb21ee3a8fce250967ac2c71aafd6d432dbb`  
		Last Modified: Thu, 15 Apr 2021 10:57:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; 386

```console
$ docker pull ghost@sha256:868a817027ffbfda2da9e1283ac4921968d27cfb20c59d203f6020aa13db5c35
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93521985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1e451ed85192f4758959d7afaaf10a483ccdd8ccd649b8d9e42ffa42a68b2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:42 GMT
ADD file:09db668d771495bb87e6b4c5fde70d7e786ab1efdc74e677aabfc1f91a9c6621 in / 
# Wed, 14 Apr 2021 18:38:42 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:42:12 GMT
ENV NODE_VERSION=10.24.1
# Thu, 15 Apr 2021 03:08:12 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="138eed35daca02bbc01cae161e13604b1b71139e9552d4cb9fe3aad742ce94ec"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 15 Apr 2021 03:08:13 GMT
ENV YARN_VERSION=1.22.5
# Thu, 15 Apr 2021 03:08:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 15 Apr 2021 03:08:17 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:08:17 GMT
CMD ["node"]
# Thu, 15 Apr 2021 08:28:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 15 Apr 2021 08:28:38 GMT
RUN apk add --no-cache 		bash
# Thu, 15 Apr 2021 08:28:39 GMT
ENV NODE_ENV=production
# Thu, 15 Apr 2021 08:28:39 GMT
ENV GHOST_CLI_VERSION=1.16.3
# Thu, 15 Apr 2021 08:28:56 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Thu, 15 Apr 2021 08:28:57 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Apr 2021 08:28:57 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Apr 2021 08:28:57 GMT
ENV GHOST_VERSION=2.38.3
# Thu, 15 Apr 2021 08:31:20 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 15 Apr 2021 08:31:21 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Apr 2021 08:31:21 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Apr 2021 08:31:21 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 15 Apr 2021 08:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:31:22 GMT
EXPOSE 2368
# Thu, 15 Apr 2021 08:31:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ac056f5820900a5fb1267696349da84ea69194da83f527e904b0f9c277c5f65d`  
		Last Modified: Wed, 14 Apr 2021 18:39:56 GMT  
		Size: 2.8 MB (2812104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bf833cba7798f71d74ca35e3912118596c737a57612328c013af2061e893c7`  
		Last Modified: Thu, 15 Apr 2021 03:09:56 GMT  
		Size: 22.4 MB (22437666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99650daa1a4d3f089856f37707f966da9830b4443381784ee942e89ae59d78`  
		Last Modified: Thu, 15 Apr 2021 03:09:51 GMT  
		Size: 2.4 MB (2368250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a40b59e62a8c55854a56d834fa68e444cc37851998fa95dda3b0912f13fe18a`  
		Last Modified: Thu, 15 Apr 2021 03:09:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08864acdeb5d8e7060c5ef8f485680f0810fd9154dbe0e10890e373b4756c1b8`  
		Last Modified: Thu, 15 Apr 2021 08:31:42 GMT  
		Size: 10.0 KB (9995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd201036d3cc0aaee6210d8f9ff7b091b8bf3e43e6fdc04bdd4732acffab2008`  
		Last Modified: Thu, 15 Apr 2021 08:31:42 GMT  
		Size: 831.2 KB (831213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33be874ebd8a5c600916db312981588599a118f990935f7e56bee995d25a036`  
		Last Modified: Thu, 15 Apr 2021 08:31:45 GMT  
		Size: 7.4 MB (7405106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c35f5f19c8fd1000f7ce8333c72a754b03a14fd07ada8121cc3df2aecba5154`  
		Last Modified: Thu, 15 Apr 2021 08:31:55 GMT  
		Size: 57.7 MB (57656827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5a90dbd206fe3a703ec3f8720043017ad9ee9aa3a77ff10607e2bb1a6aeef7`  
		Last Modified: Thu, 15 Apr 2021 08:31:42 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
