## `ghost:2-alpine`

```console
$ docker pull ghost@sha256:cb2bb94b9d61e0710dda5c5adf8f877f9a8529d39db6251948c8e12de4b6a9d3
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
$ docker pull ghost@sha256:8912ba49c508c6cb5738f31b682d0d0c2e0fb57952c0a40d388fafd14e5e0245
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107666481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223592c5ac2e686b9f04abbd0293988fcf7042bb8866e939eee7a303c65ff755`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Feb 2021 21:36:29 GMT
ENV NODE_VERSION=10.24.0
# Tue, 23 Feb 2021 21:36:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5603560113fe549eeba455cef8bffc5a857ec969b5bdd6faa85a17a654a1bf59"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 23 Feb 2021 21:36:41 GMT
ENV YARN_VERSION=1.22.5
# Tue, 23 Feb 2021 21:36:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 23 Feb 2021 21:36:47 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 23 Feb 2021 21:36:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Feb 2021 21:36:47 GMT
CMD ["node"]
# Tue, 23 Feb 2021 22:20:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 23 Feb 2021 22:20:05 GMT
RUN apk add --no-cache 		bash
# Tue, 23 Feb 2021 22:20:05 GMT
ENV NODE_ENV=production
# Tue, 23 Feb 2021 22:20:05 GMT
ENV GHOST_CLI_VERSION=1.15.3
# Tue, 23 Feb 2021 22:20:42 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 23 Feb 2021 22:20:43 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Feb 2021 22:20:43 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Feb 2021 22:20:43 GMT
ENV GHOST_VERSION=2.38.3
# Tue, 23 Feb 2021 22:22:24 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 23 Feb 2021 22:22:25 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Feb 2021 22:22:26 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Feb 2021 22:22:26 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 23 Feb 2021 22:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Feb 2021 22:22:27 GMT
EXPOSE 2368
# Tue, 23 Feb 2021 22:22:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d01549d3992c603058687daffe472a3ce4cb7f7527459d6812b8dae3ce4a96`  
		Last Modified: Tue, 23 Feb 2021 21:52:32 GMT  
		Size: 22.2 MB (22205630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35acd139872ddb44f40980fd087e935586ee80581c3563d68f7875546d7939a8`  
		Last Modified: Tue, 23 Feb 2021 21:52:28 GMT  
		Size: 2.3 MB (2344943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b37be8639d5ddcdfbdf6c3863afbd3859c416d13580867175a9cc961b22c2e`  
		Last Modified: Tue, 23 Feb 2021 21:52:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b322a89e9cf9d717586d90876e7a6700f550390f33b56d31eb2ea520c8f3f63`  
		Last Modified: Tue, 23 Feb 2021 22:24:41 GMT  
		Size: 9.9 KB (9910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d688e270407402b9708ae79a137020b3f4e3ac92179bfb9b5f1d0e50ba433ca5`  
		Last Modified: Tue, 23 Feb 2021 22:24:42 GMT  
		Size: 780.5 KB (780544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25589bfc92ec94924436b13812ab68ec9d9c7bc6019fb6b232686c536059017`  
		Last Modified: Tue, 23 Feb 2021 22:24:47 GMT  
		Size: 7.4 MB (7439460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba31d654d15d7f494565edc609d2a2d042850e5e5d028a9a262bcccc9f60ec26`  
		Last Modified: Tue, 23 Feb 2021 22:25:04 GMT  
		Size: 72.1 MB (72070300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4315d2d3adc40e6beefc4423db02e22793d92f94b99d3cfd8cd06de82c259e`  
		Last Modified: Tue, 23 Feb 2021 22:24:41 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:31c6035c0c93ac2647c52af9ed6c69fb71f2fc5f257722addc70aef71e5cf355
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92217155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7678d5a79b366b1f34a949c399ca711afd7951ce3af19789a7219b8dbba03368`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Sat, 13 Feb 2021 01:25:57 GMT
ENV NODE_VERSION=10.23.3
# Sat, 13 Feb 2021 01:33:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0f7cfb9c2b3f2f53d307756a6f824013b5c5f1cba503f55e3ecbc1653786e7b9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 13 Feb 2021 01:33:37 GMT
ENV YARN_VERSION=1.22.5
# Sat, 13 Feb 2021 01:33:43 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 13 Feb 2021 01:33:45 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 13 Feb 2021 01:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 01:33:48 GMT
CMD ["node"]
# Sat, 13 Feb 2021 02:18:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Feb 2021 02:18:06 GMT
RUN apk add --no-cache 		bash
# Sat, 13 Feb 2021 02:18:09 GMT
ENV NODE_ENV=production
# Sat, 13 Feb 2021 02:18:10 GMT
ENV GHOST_CLI_VERSION=1.15.3
# Sat, 13 Feb 2021 02:18:55 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 13 Feb 2021 02:19:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 13 Feb 2021 02:19:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 13 Feb 2021 02:19:02 GMT
ENV GHOST_VERSION=2.38.3
# Sat, 13 Feb 2021 02:24:48 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 13 Feb 2021 02:24:55 GMT
WORKDIR /var/lib/ghost
# Sat, 13 Feb 2021 02:24:55 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 13 Feb 2021 02:24:56 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 13 Feb 2021 02:24:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 02:24:57 GMT
EXPOSE 2368
# Sat, 13 Feb 2021 02:24:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713c5dc130e76af9d53e93e852b551bc633a888d38c483b9b21e0e7abda38d43`  
		Last Modified: Sat, 13 Feb 2021 01:37:49 GMT  
		Size: 21.6 MB (21646764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe8334f661d836de9c0f038eac45aaa7edd5562a38aade87fd6e7db6870778d`  
		Last Modified: Sat, 13 Feb 2021 01:37:41 GMT  
		Size: 2.4 MB (2368166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e933fdaf508045e278642aad6982f883b43aba7104b7402146e76d5766a69e`  
		Last Modified: Sat, 13 Feb 2021 01:37:40 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b08fb7bd0e768fe1c9e52dd5488f9c90d6a908b068bbde2687c732baad469bc`  
		Last Modified: Sat, 13 Feb 2021 02:26:01 GMT  
		Size: 9.7 KB (9730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1911e1db4c62ef414770a6ad598604796bd6ded7649f0486e324b9c8e0be8a1b`  
		Last Modified: Sat, 13 Feb 2021 02:26:02 GMT  
		Size: 733.5 KB (733469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763ab0d8675282f6c5bd954ba7b5b1561753e100361ebd0e16dd3f41a87a09ad`  
		Last Modified: Sat, 13 Feb 2021 02:26:07 GMT  
		Size: 7.4 MB (7438711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bcc4e6a45641217c8c819ae69f80a639af69cea7ff0ec6d206b78ab6bd7fed`  
		Last Modified: Sat, 13 Feb 2021 02:26:27 GMT  
		Size: 57.4 MB (57398718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf3a91a443238faa3deb183b9de2c8099771cc41ade8b74823a100fb3ad0fb`  
		Last Modified: Sat, 13 Feb 2021 02:26:01 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:64ca2991684b11af2e23c0adccb171447d0c8034f34c37fc664fcb7919d1d326
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91070137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be2c2b06840955a264845f2c57d2a2c18460e2ef6c7214f341b7e5c30ec1cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:28 GMT
ADD file:6757438ec5b22931a1c6a274c9c1eca94f0715a405d2ba91bd8b95704ba969ca in / 
# Wed, 16 Dec 2020 23:58:29 GMT
CMD ["/bin/sh"]
# Sat, 13 Feb 2021 01:25:46 GMT
ENV NODE_VERSION=10.23.3
# Sat, 13 Feb 2021 01:32:54 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0f7cfb9c2b3f2f53d307756a6f824013b5c5f1cba503f55e3ecbc1653786e7b9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 13 Feb 2021 01:33:01 GMT
ENV YARN_VERSION=1.22.5
# Sat, 13 Feb 2021 01:33:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 13 Feb 2021 01:33:18 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 13 Feb 2021 01:33:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 01:33:20 GMT
CMD ["node"]
# Sat, 13 Feb 2021 02:21:15 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Feb 2021 02:21:17 GMT
RUN apk add --no-cache 		bash
# Sat, 13 Feb 2021 02:21:18 GMT
ENV NODE_ENV=production
# Sat, 13 Feb 2021 02:21:19 GMT
ENV GHOST_CLI_VERSION=1.15.3
# Sat, 13 Feb 2021 02:21:51 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 13 Feb 2021 02:21:53 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 13 Feb 2021 02:21:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 13 Feb 2021 02:21:55 GMT
ENV GHOST_VERSION=2.38.3
# Sat, 13 Feb 2021 02:26:15 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 13 Feb 2021 02:26:20 GMT
WORKDIR /var/lib/ghost
# Sat, 13 Feb 2021 02:26:21 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 13 Feb 2021 02:26:22 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 13 Feb 2021 02:26:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 02:26:23 GMT
EXPOSE 2368
# Sat, 13 Feb 2021 02:26:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:71728559ce1f58d5e0ef30be5b1d7628ff967d4038f9202818dd3d8c76feb8ab`  
		Last Modified: Wed, 16 Dec 2020 23:59:11 GMT  
		Size: 2.4 MB (2422964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51220462423c2d91f80b6188e587ba84036ab99fa4e2e065b62d0cfbdead0122`  
		Last Modified: Sat, 13 Feb 2021 01:43:54 GMT  
		Size: 21.2 MB (21246651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d78966ef5a5ac936166f13c733714d5624d36a6b60087b6133c5ae69bb1f8f9`  
		Last Modified: Sat, 13 Feb 2021 01:43:47 GMT  
		Size: 2.4 MB (2368289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129576ac54c382492d27d7961e81518715b1cc4deb444b87e74aab7a0110e458`  
		Last Modified: Sat, 13 Feb 2021 01:43:46 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00a90c1a4e18f1e8bc36b7acb4f52e24dd325e992d892713db2a2b6d296713`  
		Last Modified: Sat, 13 Feb 2021 02:28:58 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa49fa819f4c5ce94aec4c76fd5e866ae6533adf923a86ed5a02da6e7704f6e`  
		Last Modified: Sat, 13 Feb 2021 02:28:58 GMT  
		Size: 669.0 KB (669044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3932e1a7d0a7af538f6c30297bff89ffde41d6e07a0d5d2ff2c9a8b73e89ba7d`  
		Last Modified: Sat, 13 Feb 2021 02:29:03 GMT  
		Size: 7.4 MB (7438504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a0f237d8aca5e4554f00187eafd4735c620f9b47ae0f2f8be59a5a537c93da`  
		Last Modified: Sat, 13 Feb 2021 02:29:21 GMT  
		Size: 56.9 MB (56914335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510dda1c115cbd1b2c7860e0cd0dba4333971a5457505c453df3e98449f437ed`  
		Last Modified: Sat, 13 Feb 2021 02:28:58 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:dc6e8fce84d543031250f6617a1efbc4c562713e433e460f13ee3abfb49b3de2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93370283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564401992ea4c08d697ee9f228803baf749b2068c97d0966d3caa87ad12c24eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Sat, 13 Feb 2021 01:21:13 GMT
ENV NODE_VERSION=10.23.3
# Sat, 13 Feb 2021 01:28:58 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="0f7cfb9c2b3f2f53d307756a6f824013b5c5f1cba503f55e3ecbc1653786e7b9"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Sat, 13 Feb 2021 01:29:02 GMT
ENV YARN_VERSION=1.22.5
# Sat, 13 Feb 2021 01:29:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 13 Feb 2021 01:29:20 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 13 Feb 2021 01:29:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 01:29:24 GMT
CMD ["node"]
# Sat, 13 Feb 2021 02:48:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Feb 2021 02:48:10 GMT
RUN apk add --no-cache 		bash
# Sat, 13 Feb 2021 02:48:11 GMT
ENV NODE_ENV=production
# Sat, 13 Feb 2021 02:48:11 GMT
ENV GHOST_CLI_VERSION=1.15.3
# Sat, 13 Feb 2021 02:48:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 13 Feb 2021 02:48:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 13 Feb 2021 02:48:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 13 Feb 2021 02:48:40 GMT
ENV GHOST_VERSION=2.38.3
# Sat, 13 Feb 2021 02:52:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 13 Feb 2021 02:53:02 GMT
WORKDIR /var/lib/ghost
# Sat, 13 Feb 2021 02:53:02 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 13 Feb 2021 02:53:03 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 13 Feb 2021 02:53:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 02:53:05 GMT
EXPOSE 2368
# Sat, 13 Feb 2021 02:53:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03b53dc708b04fed2e6482927534fb204b25d99fd47bfe56a927006c596f468`  
		Last Modified: Sat, 13 Feb 2021 01:41:52 GMT  
		Size: 22.5 MB (22464860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230e29318f85b4c48f43f5325a8296c237fd5f9d7c4225903df6e87c9964156`  
		Last Modified: Sat, 13 Feb 2021 01:41:46 GMT  
		Size: 2.4 MB (2408296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac824665ba408a8d38406e1ae2a8efabb07ce1460d145afa7a72fc4cc2dd7faf`  
		Last Modified: Sat, 13 Feb 2021 01:41:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1d4982f115b5e8134ad7add6b916d78fd9730a949c65e382320f11bccae000`  
		Last Modified: Sat, 13 Feb 2021 02:55:05 GMT  
		Size: 9.8 KB (9846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf8ee7e7386158bc1780cdd516c087e6884fc1188d2fd8e5588c22e287cf20a`  
		Last Modified: Sat, 13 Feb 2021 02:55:05 GMT  
		Size: 792.1 KB (792149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f62b9b0ad4f25298fbf5c9e81d1a062863d01e10e1c0ef7f38a2bb73f45bd0`  
		Last Modified: Sat, 13 Feb 2021 02:55:08 GMT  
		Size: 7.4 MB (7438559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e03423fdd820d577ef367ba461a1d8761ee71e50158bdd0c05130e511a340f`  
		Last Modified: Sat, 13 Feb 2021 02:55:21 GMT  
		Size: 57.5 MB (57530530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a573bd38446c537ec8b5853764fbb16a6517975d423f5ebcd15aec1ba013f2`  
		Last Modified: Sat, 13 Feb 2021 02:55:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:2-alpine` - linux; 386

```console
$ docker pull ghost@sha256:079aa140859511030eb6268d8c5b62f82c6aac4ae77f52c773b4616ac1caa5d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93556847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43abbc11461d0e1012d46eebbe814193aa566994eb8f677f238c5e048694ba6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:39 GMT
ADD file:c8f5b26cfa9b90dfe6ca805f2101bd199c87b93faed2af74df0cbe54ea28fa6d in / 
# Thu, 17 Dec 2020 00:38:39 GMT
CMD ["/bin/sh"]
# Tue, 23 Feb 2021 21:53:20 GMT
ENV NODE_VERSION=10.24.0
# Tue, 23 Feb 2021 22:26:37 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="5603560113fe549eeba455cef8bffc5a857ec969b5bdd6faa85a17a654a1bf59"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 23 Feb 2021 22:26:38 GMT
ENV YARN_VERSION=1.22.5
# Tue, 23 Feb 2021 22:26:41 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 23 Feb 2021 22:26:41 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 23 Feb 2021 22:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Feb 2021 22:26:42 GMT
CMD ["node"]
# Tue, 23 Feb 2021 22:43:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 23 Feb 2021 22:43:49 GMT
RUN apk add --no-cache 		bash
# Tue, 23 Feb 2021 22:43:49 GMT
ENV NODE_ENV=production
# Tue, 23 Feb 2021 22:43:50 GMT
ENV GHOST_CLI_VERSION=1.15.3
# Tue, 23 Feb 2021 22:44:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Tue, 23 Feb 2021 22:44:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 23 Feb 2021 22:44:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 23 Feb 2021 22:44:12 GMT
ENV GHOST_VERSION=2.38.3
# Tue, 23 Feb 2021 22:47:08 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps g++ gcc libc-dev make python3 vips-dev; 				npm_config_python='python3' su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Tue, 23 Feb 2021 22:47:09 GMT
WORKDIR /var/lib/ghost
# Tue, 23 Feb 2021 22:47:09 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 23 Feb 2021 22:47:09 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Tue, 23 Feb 2021 22:47:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Feb 2021 22:47:10 GMT
EXPOSE 2368
# Tue, 23 Feb 2021 22:47:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:60519712d04c07db59906a2e14fa87c037b6504d612ba116ea1ef94ae08a650b`  
		Last Modified: Thu, 17 Dec 2020 00:39:32 GMT  
		Size: 2.8 MB (2810512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf3b44ad4896119d4dc651457372f99e76a187f95d7f5945048557e9401b9c`  
		Last Modified: Tue, 23 Feb 2021 22:27:27 GMT  
		Size: 22.4 MB (22439877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe355c0f12fc3fba95c4e5ea4583719e7dc3746e943b45ea5d457233afd0701`  
		Last Modified: Tue, 23 Feb 2021 22:27:21 GMT  
		Size: 2.4 MB (2368147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449f909c8332e88d51b6b3836172da948d9dd320389662d164fc4d7927393c37`  
		Last Modified: Tue, 23 Feb 2021 22:27:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febcee5fce330e614becc6a8a675b49e2d9d100705e90370b8e713e88437bf06`  
		Last Modified: Tue, 23 Feb 2021 22:47:25 GMT  
		Size: 10.0 KB (9982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5004ef7965ea8c5623cdea964c3f5e824a3718bb9b8ff977b904d6863413dea8`  
		Last Modified: Tue, 23 Feb 2021 22:47:26 GMT  
		Size: 831.1 KB (831097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ed5f628fc194571e136dde8271b76e2c4cfac42395f49654123cbb9d680161`  
		Last Modified: Tue, 23 Feb 2021 22:47:29 GMT  
		Size: 7.4 MB (7438722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d85f2cf23498323e65b3c6abbf3e7a7bb5285b227c2afc4b06552268b98a0f`  
		Last Modified: Tue, 23 Feb 2021 22:47:42 GMT  
		Size: 57.7 MB (57657687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4c6006607d75faf93446f19b791d471f27d0bb704702d4fec278c0e540e554`  
		Last Modified: Tue, 23 Feb 2021 22:47:25 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
