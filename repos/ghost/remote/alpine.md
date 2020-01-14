## `ghost:alpine`

```console
$ docker pull ghost@sha256:ceb09c00eba93bc899e8b6d6f8e0dd8f784d40aa2a980b728dfb2ae61a6aff54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:7e8117dd2e276f70a039d6c99f16deb1897c92f7246acec7e453464930eef2b4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112343078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc46f6c8d81d44f6924cbcb16cb3db515e9ed49533d2b043f1b89f90aa6ef87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2020 21:28:47 GMT
ENV NODE_VERSION=10.18.1
# Mon, 13 Jan 2020 21:28:51 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Mon, 13 Jan 2020 21:28:52 GMT
ENV YARN_VERSION=1.21.1
# Mon, 13 Jan 2020 21:28:54 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Mon, 13 Jan 2020 21:28:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Mon, 13 Jan 2020 21:28:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 21:28:55 GMT
CMD ["node"]
# Mon, 13 Jan 2020 21:47:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 13 Jan 2020 21:47:24 GMT
RUN apk add --no-cache 		bash
# Mon, 13 Jan 2020 21:47:24 GMT
ENV NODE_ENV=production
# Mon, 13 Jan 2020 21:47:25 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Mon, 13 Jan 2020 21:47:51 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 13 Jan 2020 21:47:52 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 13 Jan 2020 21:47:52 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 13 Jan 2020 21:47:52 GMT
ENV GHOST_VERSION=3.2.0
# Mon, 13 Jan 2020 21:49:38 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 13 Jan 2020 21:49:40 GMT
WORKDIR /var/lib/ghost
# Mon, 13 Jan 2020 21:49:40 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 13 Jan 2020 21:49:41 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 13 Jan 2020 21:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 21:49:41 GMT
EXPOSE 2368
# Mon, 13 Jan 2020 21:49:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61f5c8e5c412610548b3bb21a6df8ef900542fe8a6d0af181277eb6c82ca361`  
		Last Modified: Mon, 13 Jan 2020 21:31:35 GMT  
		Size: 22.5 MB (22525491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e0ee3b4fe78b78ee823b6c7192402a3dbb659cc9d8a8bb343829c08266932`  
		Last Modified: Mon, 13 Jan 2020 21:31:31 GMT  
		Size: 1.3 MB (1264626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcea321a82d385460fabfda1fed9227ebfc0d028574b10507681166db5abb4c`  
		Last Modified: Mon, 13 Jan 2020 21:31:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250cf73f42d5c5bcd8de23090d3fd62c51b22a298ee7c834b50965005e342d06`  
		Last Modified: Mon, 13 Jan 2020 21:52:29 GMT  
		Size: 9.9 KB (9907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e545aeaaec833d3ce798e8c7f5f50762e00a6ef07fe81c4d738cbafd15e54b6c`  
		Last Modified: Mon, 13 Jan 2020 21:52:31 GMT  
		Size: 1.2 MB (1211044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2529bd0a1f50ae0beaac97e3faa5b36591c5a08201e174f478cf65a065ac2e8`  
		Last Modified: Mon, 13 Jan 2020 21:52:39 GMT  
		Size: 6.8 MB (6815356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1474860f70eed1b22f1bce106988a46f08d1e73488100da18cc64bf729c9a`  
		Last Modified: Mon, 13 Jan 2020 21:52:59 GMT  
		Size: 77.7 MB (77714050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e01d6e0650752bc211800865d3e8569624895ab38dbb49673199986b933198`  
		Last Modified: Mon, 13 Jan 2020 21:52:28 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:20889be43bd910d976ec7f12b28813f0595e80d173cafdea269dff0743a77a39
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103770503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567579cb1dee4960b8b518b825b6ed7ffad1e4a181d71d7b32bb4b739d8d711f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2020 22:16:58 GMT
ENV NODE_VERSION=10.18.1
# Mon, 13 Jan 2020 22:23:19 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Mon, 13 Jan 2020 22:23:21 GMT
ENV YARN_VERSION=1.21.1
# Mon, 13 Jan 2020 22:23:30 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Mon, 13 Jan 2020 22:23:32 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Mon, 13 Jan 2020 22:23:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 22:23:34 GMT
CMD ["node"]
# Mon, 13 Jan 2020 22:40:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 13 Jan 2020 22:40:55 GMT
RUN apk add --no-cache 		bash
# Mon, 13 Jan 2020 22:40:56 GMT
ENV NODE_ENV=production
# Mon, 13 Jan 2020 22:40:58 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Mon, 13 Jan 2020 22:41:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 13 Jan 2020 22:41:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 13 Jan 2020 22:41:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 13 Jan 2020 22:41:39 GMT
ENV GHOST_VERSION=3.2.0
# Mon, 13 Jan 2020 22:47:41 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 13 Jan 2020 22:47:45 GMT
WORKDIR /var/lib/ghost
# Mon, 13 Jan 2020 22:47:45 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 13 Jan 2020 22:47:46 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 13 Jan 2020 22:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 22:47:47 GMT
EXPOSE 2368
# Mon, 13 Jan 2020 22:47:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38848baf3a81838bb0c84c089347d2471cd4176fbcdff7993c597be8700f6228`  
		Last Modified: Mon, 13 Jan 2020 22:25:16 GMT  
		Size: 22.0 MB (21986814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c981a6cf8efe2bfbc393daa3da55a20c5523a6b5040bf363855d95e366b9ef`  
		Last Modified: Mon, 13 Jan 2020 22:25:05 GMT  
		Size: 1.3 MB (1327786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a7672b81c272faaf27661dcfd633e4642728c8b0914c73fc1a1e31ae92896e`  
		Last Modified: Mon, 13 Jan 2020 22:25:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7465617262858be4cafd1288f18950f29a6eff5583f8d71f9d15f9cc1fc1c9c1`  
		Last Modified: Mon, 13 Jan 2020 22:54:22 GMT  
		Size: 9.7 KB (9730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9af624a5b2662c08f12494d448adaf6f889ea2e43a92d4723f323b8b38d84`  
		Last Modified: Mon, 13 Jan 2020 22:54:23 GMT  
		Size: 1.2 MB (1162964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa5776ff1a64cb51debe73012e701e49f33c0dd9a1a3e3f37282cafbe76c1e1`  
		Last Modified: Mon, 13 Jan 2020 22:54:28 GMT  
		Size: 6.8 MB (6815384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec38af4296a7c7e7ac2c485d28e15ec0579a3b3576813da91b7858bdfb755d9`  
		Last Modified: Mon, 13 Jan 2020 22:54:49 GMT  
		Size: 69.9 MB (69854983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2448f78c430b936b42bf580b77f80687377682f719853926a28cc58da9315027`  
		Last Modified: Mon, 13 Jan 2020 22:54:22 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:06bf7c9de784ef12c317bb0b5b5c231c6e75409152315231ce411100fd96490b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102180706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b9b3c700ca1b83e5dc8e78ffe6b3c44391f2252eebd6fcc03245ea4d096e73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2020 22:33:29 GMT
ENV NODE_VERSION=10.18.1
# Mon, 13 Jan 2020 22:38:33 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Mon, 13 Jan 2020 22:38:34 GMT
ENV YARN_VERSION=1.21.1
# Mon, 13 Jan 2020 22:38:39 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Mon, 13 Jan 2020 22:38:40 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Mon, 13 Jan 2020 22:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 22:38:41 GMT
CMD ["node"]
# Mon, 13 Jan 2020 23:09:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 13 Jan 2020 23:09:53 GMT
RUN apk add --no-cache 		bash
# Mon, 13 Jan 2020 23:09:54 GMT
ENV NODE_ENV=production
# Mon, 13 Jan 2020 23:09:54 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Mon, 13 Jan 2020 23:10:20 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 13 Jan 2020 23:10:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 13 Jan 2020 23:10:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 13 Jan 2020 23:10:23 GMT
ENV GHOST_VERSION=3.2.0
# Mon, 13 Jan 2020 23:14:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 13 Jan 2020 23:14:48 GMT
WORKDIR /var/lib/ghost
# Mon, 13 Jan 2020 23:14:49 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 13 Jan 2020 23:14:50 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 13 Jan 2020 23:14:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 23:14:51 GMT
EXPOSE 2368
# Mon, 13 Jan 2020 23:14:52 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b88ecf62890cf46e174c16e7b0a402bfeb7566eefc12970f4ff2dec1eed6a4`  
		Last Modified: Mon, 13 Jan 2020 22:42:49 GMT  
		Size: 21.6 MB (21588693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e5c22e100ad8b1a6985e19c8c592eda12d520b55694a51968949132f8cf1dd`  
		Last Modified: Mon, 13 Jan 2020 22:42:41 GMT  
		Size: 1.3 MB (1327723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a82debc1e0303fc607f41d4eecd9bd56ee1ab7d3187ca41cefc1c27f380db7`  
		Last Modified: Mon, 13 Jan 2020 22:42:41 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b246dadd49d4c2ee7e69e71a1f5b29502d14a1ee7e8abde7595a14a671e91aac`  
		Last Modified: Mon, 13 Jan 2020 23:20:10 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56b64a3601d1148fea67385ca040f29f71a47c5bb47a1935cc6c0903a7924bd`  
		Last Modified: Mon, 13 Jan 2020 23:20:11 GMT  
		Size: 1.1 MB (1101455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617c8eb4b08ff5d5446fdab018f28b6153ffb1c7b2d6a041925243cfc359b293`  
		Last Modified: Mon, 13 Jan 2020 23:20:15 GMT  
		Size: 6.8 MB (6815264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93633ffe73de8242259ad68e75f7ddce788976c8d6ccfbfb4f602851cd425bb1`  
		Last Modified: Mon, 13 Jan 2020 23:20:36 GMT  
		Size: 68.9 MB (68920541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697c58c25a427f6d2c7ca224a26de30b7c2565accb52cb7489f2ffdb7c4a6fbd`  
		Last Modified: Mon, 13 Jan 2020 23:20:10 GMT  
		Size: 540.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:352e3c35521eb09834e8023436cdaede03536b1b2d97ce5c7c7dd984a764c77a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105049215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48df3719ac3680fe2065d4125e14adef462cebcd5950a4450a4e1300a9fa8cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 20:26:15 GMT
ADD file:d6c3db0313ab0c6201770c7248d1bac964011a1c08f1a9b434442b7c21efef87 in / 
# Tue, 24 Dec 2019 20:26:24 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2020 21:57:33 GMT
ENV NODE_VERSION=10.18.1
# Mon, 13 Jan 2020 22:04:38 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Mon, 13 Jan 2020 22:04:43 GMT
ENV YARN_VERSION=1.21.1
# Mon, 13 Jan 2020 22:04:52 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Mon, 13 Jan 2020 22:04:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Mon, 13 Jan 2020 22:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 22:04:57 GMT
CMD ["node"]
# Mon, 13 Jan 2020 22:27:17 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 13 Jan 2020 22:27:23 GMT
RUN apk add --no-cache 		bash
# Mon, 13 Jan 2020 22:27:25 GMT
ENV NODE_ENV=production
# Mon, 13 Jan 2020 22:27:27 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Mon, 13 Jan 2020 22:27:59 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 13 Jan 2020 22:28:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 13 Jan 2020 22:28:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 13 Jan 2020 22:28:02 GMT
ENV GHOST_VERSION=3.2.0
# Mon, 13 Jan 2020 22:33:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 13 Jan 2020 22:33:07 GMT
WORKDIR /var/lib/ghost
# Mon, 13 Jan 2020 22:33:08 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 13 Jan 2020 22:33:08 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 13 Jan 2020 22:33:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 22:33:10 GMT
EXPOSE 2368
# Mon, 13 Jan 2020 22:33:11 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cde5963f3b93eec667cad527c99d80402a5a91a7a1381f7ffe562f215aec0c50`  
		Last Modified: Tue, 24 Dec 2019 20:26:52 GMT  
		Size: 2.7 MB (2719182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04d5914ec774cba8d06ffbbb2d12cb18da1c954c6dede3adc3860c444ff3666`  
		Last Modified: Mon, 13 Jan 2020 22:09:20 GMT  
		Size: 22.8 MB (22814100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e2e0588df7fd530296242f1360713b03789315b15d6bd632fcf827a319887d`  
		Last Modified: Mon, 13 Jan 2020 22:09:10 GMT  
		Size: 1.3 MB (1327781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f8b3f060993c993fc346896e6a9f94967bd1de176141d783a3a6e7489489c4`  
		Last Modified: Mon, 13 Jan 2020 22:09:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794efcd239343916acd114bbeb3c29df16f846b8c2b372e5d534f42b1e6fff18`  
		Last Modified: Mon, 13 Jan 2020 22:39:06 GMT  
		Size: 9.8 KB (9847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47238159147d9462b0e7fefb0b5bbc74dc190e809585cd4854d465683ffb4204`  
		Last Modified: Mon, 13 Jan 2020 22:39:06 GMT  
		Size: 1.2 MB (1223198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5803dd304367fcce95aaa6fede88d7fa0163791398a72c4aee0a92478704af5`  
		Last Modified: Mon, 13 Jan 2020 22:39:10 GMT  
		Size: 6.8 MB (6815469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae8f51e0114373a3d6bbaa7bc0f26d0adcc306bdc0cc5de2bf7b715b333f1f2`  
		Last Modified: Mon, 13 Jan 2020 22:39:28 GMT  
		Size: 70.1 MB (70138814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ea62cecc2ec1f2ccbeb30899b22f0b4e5ff3375c4213c564c4f7cdae71bca3`  
		Last Modified: Mon, 13 Jan 2020 22:39:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; 386

```console
$ docker pull ghost@sha256:a631e6bd84de38f45aa28c99c1f7f5f892f67618b2ed77f69d507f7247b7173b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105316428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885e4a4c4ef62ed6047ca6a0e9b158b5d0cd52111319717bf252e3fc0bdd03e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2020 22:36:12 GMT
ENV NODE_VERSION=10.18.1
# Mon, 13 Jan 2020 23:05:02 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Mon, 13 Jan 2020 23:05:03 GMT
ENV YARN_VERSION=1.21.1
# Mon, 13 Jan 2020 23:05:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Mon, 13 Jan 2020 23:05:05 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Mon, 13 Jan 2020 23:05:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 23:05:06 GMT
CMD ["node"]
# Mon, 13 Jan 2020 23:21:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 13 Jan 2020 23:21:27 GMT
RUN apk add --no-cache 		bash
# Mon, 13 Jan 2020 23:21:27 GMT
ENV NODE_ENV=production
# Mon, 13 Jan 2020 23:21:27 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Mon, 13 Jan 2020 23:21:43 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 13 Jan 2020 23:21:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 13 Jan 2020 23:21:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 13 Jan 2020 23:21:44 GMT
ENV GHOST_VERSION=3.2.0
# Mon, 13 Jan 2020 23:24:38 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 13 Jan 2020 23:24:39 GMT
WORKDIR /var/lib/ghost
# Mon, 13 Jan 2020 23:24:40 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 13 Jan 2020 23:24:40 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 13 Jan 2020 23:24:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 23:24:40 GMT
EXPOSE 2368
# Mon, 13 Jan 2020 23:24:40 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d767bcc74d97e87b57a779558ae7781517d923de8bf6a8678a740e11df134b10`  
		Last Modified: Mon, 13 Jan 2020 23:06:03 GMT  
		Size: 22.8 MB (22776719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423c7579e96bca7a04bff2564fe17e32f07fc711c00b5c07b61f00f5e4d5b7e`  
		Last Modified: Mon, 13 Jan 2020 23:05:57 GMT  
		Size: 1.3 MB (1327776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c558c5ca898887a4dfd1c36d4af4e2f9dac7cf0f450c1e671d7868f39981dee2`  
		Last Modified: Mon, 13 Jan 2020 23:05:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d323237312cfe5360fc2f29ae21dc80e4985f7c4d234565df510c5f8894fcd07`  
		Last Modified: Mon, 13 Jan 2020 23:28:11 GMT  
		Size: 10.0 KB (9989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ddd7778632c3477fc9590c64b98e66bbb65b20ff76719089c4574317df3c46`  
		Last Modified: Mon, 13 Jan 2020 23:28:11 GMT  
		Size: 1.3 MB (1261260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fc1a5e9e21891535914c1787a2bb03fbef34ab5aed155ca223b0310bdb0c47`  
		Last Modified: Mon, 13 Jan 2020 23:28:15 GMT  
		Size: 6.8 MB (6815075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad722d8bf5b114b556e77a6bab3695c1dc2979a6a00328a9787f65a8c19b025f`  
		Last Modified: Mon, 13 Jan 2020 23:28:29 GMT  
		Size: 70.3 MB (70319641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04354c74dbcf8f86043342340bc4f2dc8ba836a4bf4ac505f50b84259ebd75e0`  
		Last Modified: Mon, 13 Jan 2020 23:28:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; ppc64le

```console
$ docker pull ghost@sha256:45982f034d44b9304151dab844221a4e69e12ee29fb09a4ad9d2712f03b8f4bd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108726440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d99771dc8d834d40226e8fd6de300bda18550c68bd22b765faa3d4e548510e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2020 21:58:34 GMT
ENV NODE_VERSION=10.18.1
# Mon, 13 Jan 2020 22:10:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Mon, 13 Jan 2020 22:10:51 GMT
ENV YARN_VERSION=1.21.1
# Mon, 13 Jan 2020 22:10:59 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Mon, 13 Jan 2020 22:11:00 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Mon, 13 Jan 2020 22:11:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 22:11:03 GMT
CMD ["node"]
# Mon, 13 Jan 2020 22:32:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 13 Jan 2020 22:32:42 GMT
RUN apk add --no-cache 		bash
# Mon, 13 Jan 2020 22:32:44 GMT
ENV NODE_ENV=production
# Mon, 13 Jan 2020 22:32:47 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Mon, 13 Jan 2020 22:33:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 13 Jan 2020 22:33:18 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 13 Jan 2020 22:33:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 13 Jan 2020 22:33:24 GMT
ENV GHOST_VERSION=3.2.0
# Mon, 13 Jan 2020 22:37:10 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 13 Jan 2020 22:37:19 GMT
WORKDIR /var/lib/ghost
# Mon, 13 Jan 2020 22:37:22 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 13 Jan 2020 22:37:23 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 13 Jan 2020 22:37:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 22:37:28 GMT
EXPOSE 2368
# Mon, 13 Jan 2020 22:37:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef107845d87184406de3a63202e4b3a5d22b095a896b66078ed804612e5eab42`  
		Last Modified: Mon, 13 Jan 2020 22:16:11 GMT  
		Size: 24.5 MB (24534745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3e330ff0edfc2a343d2aceea38416da516ae1f820dda30dcffb6c24d2e9841`  
		Last Modified: Mon, 13 Jan 2020 22:16:06 GMT  
		Size: 1.3 MB (1327805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faa4230e538cf8add8c642e92765d7b23aa20dca03f2f6aea8ef0e8705d0097`  
		Last Modified: Mon, 13 Jan 2020 22:16:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4f97d077bf81390b27c381302920af1d1dff971a48a9c13ae852e4927b3ac4`  
		Last Modified: Mon, 13 Jan 2020 22:42:41 GMT  
		Size: 10.4 KB (10399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c524d69965eea56e41dc83c68009564b75a401cafaa2aad0616edab90b9cf1`  
		Last Modified: Mon, 13 Jan 2020 22:42:44 GMT  
		Size: 1.3 MB (1293109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07783c440d94d7e7acd2a25eec0a3b1ccd8f18f439f0e2ed5a3bfd9a0f87267`  
		Last Modified: Mon, 13 Jan 2020 22:43:03 GMT  
		Size: 6.8 MB (6815229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e85947459ea182206d9fe699869f55e3f16e3bd10bf57dcb7530dd0a3d243e1`  
		Last Modified: Mon, 13 Jan 2020 22:43:28 GMT  
		Size: 71.9 MB (71927846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05100192e4b83c24ca7e33a73c6839e1f0d501df790b3c3f469d129a37c5cc34`  
		Last Modified: Mon, 13 Jan 2020 22:42:40 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; s390x

```console
$ docker pull ghost@sha256:19e41a1a97f6badfce4dde7769fd67d4c95adc9ab5be0a8965af11c3dd0b512f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104519944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75968cf7cd0066f37a2757e3d639ae9236dfd4fa582b7d95abc864da6b29b20a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 24 Dec 2019 20:16:56 GMT
ADD file:d26fbcd308b78da175af74382b16ee1f7a3370ab9d618b306d604d292e72c560 in / 
# Tue, 24 Dec 2019 20:16:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2020 22:13:32 GMT
ENV NODE_VERSION=10.18.1
# Mon, 13 Jan 2020 22:24:38 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Mon, 13 Jan 2020 22:24:38 GMT
ENV YARN_VERSION=1.21.1
# Mon, 13 Jan 2020 22:24:40 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Mon, 13 Jan 2020 22:24:40 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Mon, 13 Jan 2020 22:24:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 22:24:41 GMT
CMD ["node"]
# Mon, 13 Jan 2020 22:51:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 13 Jan 2020 22:51:51 GMT
RUN apk add --no-cache 		bash
# Mon, 13 Jan 2020 22:51:51 GMT
ENV NODE_ENV=production
# Mon, 13 Jan 2020 22:51:52 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Mon, 13 Jan 2020 22:52:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 13 Jan 2020 22:52:02 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 13 Jan 2020 22:52:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 13 Jan 2020 22:52:02 GMT
ENV GHOST_VERSION=3.2.0
# Mon, 13 Jan 2020 22:53:43 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 13 Jan 2020 22:53:44 GMT
WORKDIR /var/lib/ghost
# Mon, 13 Jan 2020 22:53:44 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 13 Jan 2020 22:53:45 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 13 Jan 2020 22:53:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2020 22:53:45 GMT
EXPOSE 2368
# Mon, 13 Jan 2020 22:53:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bca389ebb9be8103bf737251d68f962104771b2f9c1fff1f7ae0207458fa4c86`  
		Last Modified: Tue, 24 Dec 2019 20:17:18 GMT  
		Size: 2.6 MB (2579591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b0400c4de02d58df5ffe3e4f7b51324b6bcf6161e49e71f3330e0393a74676`  
		Last Modified: Mon, 13 Jan 2020 22:26:51 GMT  
		Size: 22.6 MB (22597821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0399ab427cca69ad0e1af45a0f122c465fa10c9f9f9b97aec6abab02df4f47a`  
		Last Modified: Mon, 13 Jan 2020 22:26:48 GMT  
		Size: 1.3 MB (1327658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec71dedfe1d5baceb42fcc612ead7ecfaa933087931d2b48a9668f2e38fbfaa0`  
		Last Modified: Mon, 13 Jan 2020 22:26:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ad091bf55d568a0effe964e43d97023620cc613d711435c7560d6f99671808`  
		Last Modified: Mon, 13 Jan 2020 22:56:17 GMT  
		Size: 10.0 KB (9992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf606404a1f8c102dba795963d55920d1cc1d63e4f729c6dfc6f7c4b3ff97b7`  
		Last Modified: Mon, 13 Jan 2020 22:56:18 GMT  
		Size: 1.2 MB (1245190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cd415b0e25422382c1548b42375c5eb80fbe5791810e9d57f14e751183b6f`  
		Last Modified: Mon, 13 Jan 2020 22:56:19 GMT  
		Size: 6.8 MB (6814826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479b4c4948aa54087308967ea24a60a8bd720ef9b7d980c5046efdb71548b656`  
		Last Modified: Mon, 13 Jan 2020 22:56:27 GMT  
		Size: 69.9 MB (69944042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca75a8f7adaa8336d2195db44ebd0e8a7f330be35a81f0cbee3beae1406bb038`  
		Last Modified: Mon, 13 Jan 2020 22:56:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
