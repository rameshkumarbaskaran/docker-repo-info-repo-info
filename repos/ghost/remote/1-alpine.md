## `ghost:1-alpine`

```console
$ docker pull ghost@sha256:e26854656ee5f3a2dcd814031bc63c2dfbada07e2b1324863822b4612e023f48
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

### `ghost:1-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:56fa8fc9749d8add48bf9bbb20b38a6469fd02720ba023458ab7bd1963304bcc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85995145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be8fa943fed9c9eb39c23565c5c8f62b249598273166b7d5fb3ac09da7ec1da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:23:14 GMT
ENV NODE_VERSION=10.18.1
# Sat, 18 Jan 2020 04:23:19 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Sat, 18 Jan 2020 04:23:19 GMT
ENV YARN_VERSION=1.21.1
# Sat, 18 Jan 2020 04:23:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Sat, 18 Jan 2020 04:23:22 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:23:22 GMT
CMD ["node"]
# Sat, 18 Jan 2020 06:15:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 18 Jan 2020 06:15:06 GMT
RUN apk add --no-cache 		bash
# Sat, 18 Jan 2020 06:15:06 GMT
ENV NODE_ENV=production
# Sat, 18 Jan 2020 06:15:07 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 18 Jan 2020 06:15:32 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 18 Jan 2020 06:15:33 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 18 Jan 2020 06:15:33 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 18 Jan 2020 06:17:22 GMT
ENV GHOST_VERSION=1.26.2
# Sat, 18 Jan 2020 06:18:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 18 Jan 2020 06:18:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 18 Jan 2020 06:18:17 GMT
WORKDIR /var/lib/ghost
# Sat, 18 Jan 2020 06:18:18 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 18 Jan 2020 06:18:18 GMT
COPY file:f1f79dab1b0ea9368239b43e3c806a8db315a341a8f204dd7b9a889f2526129f in /usr/local/bin 
# Sat, 18 Jan 2020 06:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 06:18:18 GMT
EXPOSE 2368
# Sat, 18 Jan 2020 06:18:18 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa52e824d88de3c442d42f45ced6606431c19b324d2985c3b15a565ee94bd98`  
		Last Modified: Sat, 18 Jan 2020 04:24:51 GMT  
		Size: 22.5 MB (22525822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c02285c2c3ab7900d579060164ac7aaad75583b9994b4e6bbd1cf031045140`  
		Last Modified: Sat, 18 Jan 2020 04:24:46 GMT  
		Size: 1.3 MB (1264621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bf867b98a5303bd9a1d6841169ce11f0aaca4f6cc541b79f98577fd1f631`  
		Last Modified: Sat, 18 Jan 2020 04:24:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6882bd751f443324d3145774f9a438f0a6dc08ee815c563b6e4b0b6450a1186`  
		Last Modified: Sat, 18 Jan 2020 06:19:03 GMT  
		Size: 9.9 KB (9904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b91e34731af50d93616d0de1deb7dbe74bda9dbc081522c02ee1ac1d25d0dbe`  
		Last Modified: Sat, 18 Jan 2020 06:19:04 GMT  
		Size: 1.2 MB (1211049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa04cf1aad3ca49d6d8508e54c9d7f776fa7a4f6e12a3b67570abf8e395941f`  
		Last Modified: Sat, 18 Jan 2020 06:19:06 GMT  
		Size: 6.8 MB (6791426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff0abf0d47812ab206c672ae11d5010ad8e8ef3e75bd6853fa60e27ebc02f8a`  
		Last Modified: Sat, 18 Jan 2020 06:19:37 GMT  
		Size: 51.4 MB (51388507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e5596626d0af252c1a87629b54618332031c57648e02de7ae06b0839e600c`  
		Last Modified: Sat, 18 Jan 2020 06:19:26 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:ab615596406086f1f80182e93ac457ba3e218018d26cadedd2410edcf748a282
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99880632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c60f7a9dd050dbc99e51a1c2831301814ba40d657fcb0eca4dd3fc7cac139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 06:17:05 GMT
ENV NODE_VERSION=10.18.1
# Sat, 18 Jan 2020 06:23:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Sat, 18 Jan 2020 06:23:27 GMT
ENV YARN_VERSION=1.21.1
# Sat, 18 Jan 2020 06:23:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Sat, 18 Jan 2020 06:23:32 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 18 Jan 2020 06:23:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 06:23:34 GMT
CMD ["node"]
# Sat, 18 Jan 2020 09:03:19 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 18 Jan 2020 09:03:36 GMT
RUN apk add --no-cache 		bash
# Sat, 18 Jan 2020 09:03:53 GMT
ENV NODE_ENV=production
# Sat, 18 Jan 2020 09:04:00 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 18 Jan 2020 09:04:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 18 Jan 2020 09:04:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 18 Jan 2020 09:05:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 18 Jan 2020 09:11:20 GMT
ENV GHOST_VERSION=1.26.2
# Sat, 18 Jan 2020 09:17:04 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 18 Jan 2020 09:17:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 18 Jan 2020 09:17:09 GMT
WORKDIR /var/lib/ghost
# Sat, 18 Jan 2020 09:17:09 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 18 Jan 2020 09:17:10 GMT
COPY file:f1f79dab1b0ea9368239b43e3c806a8db315a341a8f204dd7b9a889f2526129f in /usr/local/bin 
# Sat, 18 Jan 2020 09:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 09:17:11 GMT
EXPOSE 2368
# Sat, 18 Jan 2020 09:17:11 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf9716f29f2b96698fac52f44511edaea602c86e644f8ae93101d884d7c93e2`  
		Last Modified: Sat, 18 Jan 2020 06:25:00 GMT  
		Size: 22.0 MB (21986775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb2adc2bf9812c26f147772ca13bd65f0777de09016d51efac76dff37abf53c`  
		Last Modified: Sat, 18 Jan 2020 06:24:53 GMT  
		Size: 1.3 MB (1327775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781478f0de2d9b94843194a9e27f179c9b41ebab54a150080b7bf21829eb7067`  
		Last Modified: Sat, 18 Jan 2020 06:24:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97489847bf786aa85ea12756d9afb60fb46016f0d97a0f5133ee4ede91c6a8e`  
		Last Modified: Sat, 18 Jan 2020 09:18:15 GMT  
		Size: 9.7 KB (9732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80d09b012e4c23a7ad0e4fb7dac9affbd305d4fd45bca414610db2a4c9975e4`  
		Last Modified: Sat, 18 Jan 2020 09:18:15 GMT  
		Size: 1.2 MB (1162965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db9754e1a1be1801ca8e2b174f5b0e61b6dff7e003a5d005943a6e2c40cac16`  
		Last Modified: Sat, 18 Jan 2020 09:18:20 GMT  
		Size: 6.8 MB (6791487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45848021fa7a4187d3a8219c29ac5a833b95dae14798a750540a6ac55ad07d5a`  
		Last Modified: Sat, 18 Jan 2020 09:19:12 GMT  
		Size: 66.0 MB (65983480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513c33f0aa47224fe69f0a7af15c66cb84c5b64458e6c30c1ea70419af896615`  
		Last Modified: Sat, 18 Jan 2020 09:18:48 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:90dedc5728fda9f17de19a4de517512199b5e3f6e525bec832fd2de44ef64c4d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98308862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7127f7fe8900e4f43806d1f17bbde657a57f4b5e47cb569a85889f4d21d9d185`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:52:25 GMT
ENV NODE_VERSION=10.18.1
# Sat, 18 Jan 2020 02:57:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Sat, 18 Jan 2020 02:57:33 GMT
ENV YARN_VERSION=1.21.1
# Sat, 18 Jan 2020 02:57:39 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Sat, 18 Jan 2020 02:57:40 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:57:46 GMT
CMD ["node"]
# Sat, 18 Jan 2020 06:25:04 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 18 Jan 2020 06:25:07 GMT
RUN apk add --no-cache 		bash
# Sat, 18 Jan 2020 06:25:08 GMT
ENV NODE_ENV=production
# Sat, 18 Jan 2020 06:25:09 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 18 Jan 2020 06:25:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 18 Jan 2020 06:25:43 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 18 Jan 2020 06:25:52 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 18 Jan 2020 06:31:15 GMT
ENV GHOST_VERSION=1.26.2
# Sat, 18 Jan 2020 06:35:55 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 18 Jan 2020 06:36:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 18 Jan 2020 06:36:17 GMT
WORKDIR /var/lib/ghost
# Sat, 18 Jan 2020 06:36:21 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 18 Jan 2020 06:36:24 GMT
COPY file:f1f79dab1b0ea9368239b43e3c806a8db315a341a8f204dd7b9a889f2526129f in /usr/local/bin 
# Sat, 18 Jan 2020 06:36:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 06:36:34 GMT
EXPOSE 2368
# Sat, 18 Jan 2020 06:36:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6a724d7630bb783f6da22f4e64a3148d87cbe25d31db727454471cb76e1b8b`  
		Last Modified: Sat, 18 Jan 2020 03:00:07 GMT  
		Size: 21.6 MB (21588633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c148d2733c0ef19aeb9864aee951ae351da19788e2901edc7a6781b5f6406ac`  
		Last Modified: Sat, 18 Jan 2020 03:00:00 GMT  
		Size: 1.3 MB (1327793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fe8e5b24adc82f782d26125726036e8b092ed32170b6f77aa38825ed7e621b`  
		Last Modified: Sat, 18 Jan 2020 03:00:00 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3df9defd32cbb9166f22abc6f7761f4c4c3cd23f9b0977d67f0a5c742a6cb2`  
		Last Modified: Sat, 18 Jan 2020 06:37:36 GMT  
		Size: 9.5 KB (9517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff67297a992549be74ddfc6f03b364afc5456c485ebdcc2bdfc85475284e0f95`  
		Last Modified: Sat, 18 Jan 2020 06:37:36 GMT  
		Size: 1.1 MB (1101452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae63eb80fc2eacca5ef397a2e1bb551445d91d6f6cf6aed2054cacec3925333`  
		Last Modified: Sat, 18 Jan 2020 06:37:43 GMT  
		Size: 6.8 MB (6791439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2a178ac34ad14f927eb1e25bf2349dadc9c25d34fcf00e719a00f1be4be1b9`  
		Last Modified: Sat, 18 Jan 2020 06:38:31 GMT  
		Size: 65.1 MB (65069616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c13fc5c0e86e96ed743043f767c9b853266266c4ad7bbf28592bc9da1f180f5`  
		Last Modified: Sat, 18 Jan 2020 06:38:08 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ac8bfe486457b638ee3efd18c99396d17de326a035c4fa86344c511793d57c13
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101170200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c47c0e6adeaf3928a7ae8363caaf80a5140f675d909a55225cfc60a1854c824`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:32:18 GMT
ENV NODE_VERSION=10.18.1
# Sat, 18 Jan 2020 05:39:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Sat, 18 Jan 2020 05:39:02 GMT
ENV YARN_VERSION=1.21.1
# Sat, 18 Jan 2020 05:39:09 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Sat, 18 Jan 2020 05:39:10 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:39:22 GMT
CMD ["node"]
# Sat, 18 Jan 2020 09:12:51 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 18 Jan 2020 09:12:57 GMT
RUN apk add --no-cache 		bash
# Sat, 18 Jan 2020 09:12:59 GMT
ENV NODE_ENV=production
# Sat, 18 Jan 2020 09:12:59 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 18 Jan 2020 09:13:23 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 18 Jan 2020 09:13:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 18 Jan 2020 09:13:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 18 Jan 2020 09:17:56 GMT
ENV GHOST_VERSION=1.26.2
# Sat, 18 Jan 2020 09:22:17 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 18 Jan 2020 09:22:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 18 Jan 2020 09:22:21 GMT
WORKDIR /var/lib/ghost
# Sat, 18 Jan 2020 09:22:22 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 18 Jan 2020 09:22:22 GMT
COPY file:f1f79dab1b0ea9368239b43e3c806a8db315a341a8f204dd7b9a889f2526129f in /usr/local/bin 
# Sat, 18 Jan 2020 09:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 09:22:23 GMT
EXPOSE 2368
# Sat, 18 Jan 2020 09:22:24 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f30a09163ca99ff88a30daaf4ea16c683c112695cef3cde88294976ae9727f7`  
		Last Modified: Sat, 18 Jan 2020 05:41:58 GMT  
		Size: 22.8 MB (22814164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d49eb4ad6cd8c48ca3fddaf7eb7a69e081d412f2e7fd71b59ff5ae3dd33f06`  
		Last Modified: Sat, 18 Jan 2020 05:41:50 GMT  
		Size: 1.3 MB (1327799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1750b1b4a8a20c3700286332304c37cc793be9e984cb3adb209c90ed837034cd`  
		Last Modified: Sat, 18 Jan 2020 05:41:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7106afe71bf224647930f9c66d5c5eff5ebc9de2dcdaf56b177c664abfc263`  
		Last Modified: Sat, 18 Jan 2020 09:23:21 GMT  
		Size: 9.8 KB (9846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1d18747240039c7e67a684bc1b97e27ceb4fc8a8f6d8e638ef115d5da00158`  
		Last Modified: Sat, 18 Jan 2020 09:23:21 GMT  
		Size: 1.2 MB (1223216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d21fe1e806ebc9a33f2526a4ce1b487d09c5989424b9bff5715e40bb1a7286`  
		Last Modified: Sat, 18 Jan 2020 09:23:25 GMT  
		Size: 6.8 MB (6791429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba85d740ecdf5f9c3fe3c995eb7457c4ce0124b5b2aee7b5909fb37f4899e59`  
		Last Modified: Sat, 18 Jan 2020 09:24:12 GMT  
		Size: 66.3 MB (66279817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a698fb154131d6e651c7193f74c4096c5c1f65eb3d2b0cf74a8247d96020e7c0`  
		Last Modified: Sat, 18 Jan 2020 09:23:48 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1-alpine` - linux; 386

```console
$ docker pull ghost@sha256:c2f92371f28f55960ad5dabcef24c73af9b585f7a132b349be63bb171006da23
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101388602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c51559f46062f5b66800820219e6d28e8ce15a7ea5737e78f57d0c3a73c2cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 09:16:00 GMT
ENV NODE_VERSION=10.18.1
# Sat, 18 Jan 2020 09:44:53 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Sat, 18 Jan 2020 09:44:53 GMT
ENV YARN_VERSION=1.21.1
# Sat, 18 Jan 2020 09:44:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Sat, 18 Jan 2020 09:44:56 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 18 Jan 2020 09:44:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 09:44:57 GMT
CMD ["node"]
# Sat, 18 Jan 2020 11:15:39 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 18 Jan 2020 11:15:40 GMT
RUN apk add --no-cache 		bash
# Sat, 18 Jan 2020 11:15:41 GMT
ENV NODE_ENV=production
# Sat, 18 Jan 2020 11:15:41 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 18 Jan 2020 11:15:57 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 18 Jan 2020 11:15:57 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 18 Jan 2020 11:15:57 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 18 Jan 2020 11:18:53 GMT
ENV GHOST_VERSION=1.26.2
# Sat, 18 Jan 2020 11:22:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 18 Jan 2020 11:22:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 18 Jan 2020 11:22:13 GMT
WORKDIR /var/lib/ghost
# Sat, 18 Jan 2020 11:22:13 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 18 Jan 2020 11:22:14 GMT
COPY file:f1f79dab1b0ea9368239b43e3c806a8db315a341a8f204dd7b9a889f2526129f in /usr/local/bin 
# Sat, 18 Jan 2020 11:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 11:22:14 GMT
EXPOSE 2368
# Sat, 18 Jan 2020 11:22:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b3450098fabc5bfcbba585f77409943af53bc08ca1c56b19921b700c9aec05`  
		Last Modified: Sat, 18 Jan 2020 09:46:06 GMT  
		Size: 22.8 MB (22776465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acfa8310c964cdb484e379142dc5bb6cb6ce376c4f847338e572387a48265a2`  
		Last Modified: Sat, 18 Jan 2020 09:45:54 GMT  
		Size: 1.3 MB (1327722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d46abec1bddab52470323d47f9331619107fbf239bf95e5189de100b9b90d08`  
		Last Modified: Sat, 18 Jan 2020 09:45:53 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854f96c38e23af231c6de97202ab1dc86da44e87dbbff3417a64b2a4380be63a`  
		Last Modified: Sat, 18 Jan 2020 11:22:56 GMT  
		Size: 10.0 KB (9987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff30ed308334cc1714b31359b867eef6b76d211b16497b5261e4c3788ca9cc18`  
		Last Modified: Sat, 18 Jan 2020 11:22:57 GMT  
		Size: 1.3 MB (1261256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e35c67a748ff3f10d2ca52a8e9aa55e8941d8607898ee0d332f0bf66dbcbfe`  
		Last Modified: Sat, 18 Jan 2020 11:23:00 GMT  
		Size: 6.8 MB (6791444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad2782c9a8f568756b8d3986aa7d04ea60b62f577ea7c12a4ac0561b040018e`  
		Last Modified: Sat, 18 Jan 2020 11:23:34 GMT  
		Size: 66.4 MB (66414313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c1d4ad361896f5d199daeae38a58f12c631d9e6c813d0a5c7fe5ac3b3b3ec6`  
		Last Modified: Sat, 18 Jan 2020 11:23:18 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1-alpine` - linux; ppc64le

```console
$ docker pull ghost@sha256:8d4f317deb50a57679830b470ea56b3c934d15ccd79967ec14f361cad6595d4a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315f2ce1576e1735e939d775c01303671008157830a7426bd70173aabba24164`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 06:25:24 GMT
ENV NODE_VERSION=10.18.1
# Sat, 18 Jan 2020 06:39:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Sat, 18 Jan 2020 06:39:10 GMT
ENV YARN_VERSION=1.21.1
# Sat, 18 Jan 2020 06:39:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Sat, 18 Jan 2020 06:39:31 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 18 Jan 2020 06:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 06:39:44 GMT
CMD ["node"]
# Sat, 18 Jan 2020 09:39:20 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 18 Jan 2020 09:39:25 GMT
RUN apk add --no-cache 		bash
# Sat, 18 Jan 2020 09:39:30 GMT
ENV NODE_ENV=production
# Sat, 18 Jan 2020 09:39:32 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 18 Jan 2020 09:40:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 18 Jan 2020 09:40:07 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 18 Jan 2020 09:40:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 18 Jan 2020 09:44:33 GMT
ENV GHOST_VERSION=1.26.2
# Sat, 18 Jan 2020 09:48:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 18 Jan 2020 09:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 18 Jan 2020 09:48:09 GMT
WORKDIR /var/lib/ghost
# Sat, 18 Jan 2020 09:48:11 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 18 Jan 2020 09:48:12 GMT
COPY file:f1f79dab1b0ea9368239b43e3c806a8db315a341a8f204dd7b9a889f2526129f in /usr/local/bin 
# Sat, 18 Jan 2020 09:48:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 09:48:16 GMT
EXPOSE 2368
# Sat, 18 Jan 2020 09:48:18 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d53304a70c16550208d8c9376c1501eb96bb0cd8a2dec62c257b98e0cac5fe`  
		Last Modified: Sat, 18 Jan 2020 06:44:09 GMT  
		Size: 24.5 MB (24535257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8c02fac4f2f228cd35895d67d8346a9d05b167ce548386a92c06b65b505731`  
		Last Modified: Sat, 18 Jan 2020 06:44:01 GMT  
		Size: 1.3 MB (1327749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78d224e0f335ee8e7907963891b6249d137e457ff4c6a1c0a81256da91c413a`  
		Last Modified: Sat, 18 Jan 2020 06:44:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f9242011ba7a250a6f75086cb69af60e8f10c857e167995674ec9c2ae217b4`  
		Last Modified: Sat, 18 Jan 2020 09:50:22 GMT  
		Size: 10.4 KB (10393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc44a530a541e95d0e191eea71069ca0e8ad3b89c5b52dacdae2c7e802390ad3`  
		Last Modified: Sat, 18 Jan 2020 09:50:24 GMT  
		Size: 1.3 MB (1293107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4cd7bd7b98d6614ca2e433898d6ae28b7afd60821818e447711cbeebdaec6`  
		Last Modified: Sat, 18 Jan 2020 09:50:26 GMT  
		Size: 6.8 MB (6791606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4a3d15bdc46f062e34178555f4e7d4ca0360a0eecbab2abfe1acbaa0db605f`  
		Last Modified: Sat, 18 Jan 2020 09:51:07 GMT  
		Size: 68.0 MB (68012168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e8c15403e5c3687d68b324555d458285a7625a4ccc8d74712d670854d19025`  
		Last Modified: Sat, 18 Jan 2020 09:50:52 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1-alpine` - linux; s390x

```console
$ docker pull ghost@sha256:74822cb08b0d0ebb499deede6125cd801f21de98dd99dcd223efda25989e56a5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100673722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fae83f208a2cc0460d56a330f42cabcb4fa171b945df3a045531ceb6df7b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 18 Jan 2020 01:41:33 GMT
ADD file:a6f8b7d4ba199527053ef1ac710b5e318135cb6903cb9ad6fae4fe42e6ad0bf7 in / 
# Sat, 18 Jan 2020 01:41:33 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:30:10 GMT
ENV NODE_VERSION=10.18.1
# Sat, 18 Jan 2020 03:40:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="72de2f5e7826c2c13374c1d2e2a283556336c03b03507e8a6216b376a3c7693e"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Sat, 18 Jan 2020 03:40:56 GMT
ENV YARN_VERSION=1.21.1
# Sat, 18 Jan 2020 03:40:58 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Sat, 18 Jan 2020 03:40:58 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:40:58 GMT
CMD ["node"]
# Sat, 18 Jan 2020 04:05:55 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 18 Jan 2020 04:05:56 GMT
RUN apk add --no-cache 		bash
# Sat, 18 Jan 2020 04:05:57 GMT
ENV NODE_ENV=production
# Sat, 18 Jan 2020 04:05:57 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 18 Jan 2020 04:06:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 18 Jan 2020 04:06:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 18 Jan 2020 04:06:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 18 Jan 2020 04:08:17 GMT
ENV GHOST_VERSION=1.26.2
# Sat, 18 Jan 2020 04:11:39 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(node -p 'require("./package.json").optionalDependencies.sqlite3')"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 18 Jan 2020 04:11:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 18 Jan 2020 04:11:40 GMT
WORKDIR /var/lib/ghost
# Sat, 18 Jan 2020 04:11:41 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 18 Jan 2020 04:11:41 GMT
COPY file:f1f79dab1b0ea9368239b43e3c806a8db315a341a8f204dd7b9a889f2526129f in /usr/local/bin 
# Sat, 18 Jan 2020 04:11:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:11:41 GMT
EXPOSE 2368
# Sat, 18 Jan 2020 04:11:41 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:176bad61a3a435da03ec603d2bd8f7a69286d92f21f447b17f21f0bc4e085bde`  
		Last Modified: Sat, 18 Jan 2020 01:41:59 GMT  
		Size: 2.6 MB (2582031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c51d3013f6d39284debd9574b2deca880b964219895552d61d4a3e4a5094e7d`  
		Last Modified: Sat, 18 Jan 2020 03:42:22 GMT  
		Size: 22.6 MB (22597634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d96c0d2f655ecea9cecff71653f2b89ed8b90def48cae67f1638a6424f91a8`  
		Last Modified: Sat, 18 Jan 2020 03:42:14 GMT  
		Size: 1.3 MB (1327736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a8afb8c2631fd94872c27b9f0c16be0d8f517cbe0baaa6ea5bbaf875baf800`  
		Last Modified: Sat, 18 Jan 2020 03:42:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0f902ab4c54231919e51e7df29ad478fc478323f20d423e05d738b8863e99d`  
		Last Modified: Sat, 18 Jan 2020 04:12:27 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ccbf676755db0acca53d4804288dfe79f95ac0db99687626ebc7c873615775`  
		Last Modified: Sat, 18 Jan 2020 04:12:28 GMT  
		Size: 1.2 MB (1245169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e99b7f421ee3560054a66247b32e3ac99b03af5241152d2cde75cdb0952c87`  
		Last Modified: Sat, 18 Jan 2020 04:12:29 GMT  
		Size: 6.8 MB (6791233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164808117618cb1198ab047f29c5a3f83469f49d34bf2880a45a235dedea05f4`  
		Last Modified: Sat, 18 Jan 2020 04:12:53 GMT  
		Size: 66.1 MB (66119077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5897c769dd77b843751b84eb2cf2d798ab2bf23599aabb7abf4094f0994d10`  
		Last Modified: Sat, 18 Jan 2020 04:12:44 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
