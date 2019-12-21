## `ghost:3-alpine`

```console
$ docker pull ghost@sha256:9e6eb5da490dbf33860765bc0ff953b68553baeed71a35043475437a40f6f148
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

### `ghost:3-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:da0a2a4b088ca9132868bbc8f1e0c42ec0829b6a76709a4b58e08c681d8da679
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112117727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2629fea3f380792e86b92129868f3d6e7919c17263ce9526436887fdcfccc9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2019 16:31:53 GMT
ENV NODE_VERSION=10.18.0
# Wed, 18 Dec 2019 16:31:57 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 18 Dec 2019 16:31:58 GMT
ENV YARN_VERSION=1.21.1
# Wed, 18 Dec 2019 16:32:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 18 Dec 2019 16:32:00 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 18 Dec 2019 16:32:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2019 16:32:01 GMT
CMD ["node"]
# Wed, 18 Dec 2019 16:58:21 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 18 Dec 2019 16:58:24 GMT
RUN apk add --no-cache 		bash
# Wed, 18 Dec 2019 16:58:24 GMT
ENV NODE_ENV=production
# Wed, 18 Dec 2019 16:58:24 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Wed, 18 Dec 2019 16:58:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 18 Dec 2019 16:58:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 18 Dec 2019 16:58:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 19 Dec 2019 03:25:21 GMT
ENV GHOST_VERSION=3.2.0
# Thu, 19 Dec 2019 03:26:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 19 Dec 2019 03:26:29 GMT
WORKDIR /var/lib/ghost
# Thu, 19 Dec 2019 03:26:29 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 19 Dec 2019 03:26:29 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 19 Dec 2019 03:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2019 03:26:29 GMT
EXPOSE 2368
# Thu, 19 Dec 2019 03:26:30 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff64b59cc9440ac59e93503fc6fc303a0d49db3ca7a60e31c8bfdb07396192`  
		Last Modified: Wed, 18 Dec 2019 16:39:04 GMT  
		Size: 22.4 MB (22429829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4251edd6597852afee09f3ef1ce24a14815cd5b9b696300953e4386581cf0298`  
		Last Modified: Wed, 18 Dec 2019 16:39:00 GMT  
		Size: 1.3 MB (1263995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fa308999cb81de4ce2ca1db7198b0486c7128a3ad8f0edefaae14a10d8aa9d`  
		Last Modified: Wed, 18 Dec 2019 16:38:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b608d3c8d9cc7c51d137a59d0db7ed0e303c1507458f486c1f3cf8fbdea92816`  
		Last Modified: Wed, 18 Dec 2019 17:09:12 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613d48acf3938bc03d7b997165731c7e197f311c320017e49d78eb5a80051a3`  
		Last Modified: Wed, 18 Dec 2019 17:09:12 GMT  
		Size: 1.2 MB (1210556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d5cb966491aae5e838559cba2a9ab2bac106e1b25d6776396d9d03e9a66254`  
		Last Modified: Wed, 18 Dec 2019 17:09:17 GMT  
		Size: 6.8 MB (6788346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4acf8158a862a698f7fa208ff5e39ece771ebf1b8d82494568fc425188440b`  
		Last Modified: Thu, 19 Dec 2019 03:33:13 GMT  
		Size: 77.6 MB (77627411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4b5793dca838a5a7fe81ea03a4bae6b1fdae4ac8bceca8be1628cbeed58293`  
		Last Modified: Thu, 19 Dec 2019 03:32:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:094ba65df09531141bc0895ed779d5eb1f684dbd81e2c03b3c68af0097f19830
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103135641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5e2bd27081358367212f64418564640b6ee5c1451ca6b83ebbbee8304a7dcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 20 Dec 2019 00:03:15 GMT
ADD file:ec205d683a66c8a5c4a70c7ed6ff96c1b1f90b21431ffbbd1f2eb8defb3408f1 in / 
# Fri, 20 Dec 2019 00:03:16 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2019 23:09:22 GMT
ENV NODE_VERSION=10.18.0
# Fri, 20 Dec 2019 23:15:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Fri, 20 Dec 2019 23:15:47 GMT
ENV YARN_VERSION=1.21.1
# Fri, 20 Dec 2019 23:15:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Fri, 20 Dec 2019 23:15:51 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 20 Dec 2019 23:15:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2019 23:15:53 GMT
CMD ["node"]
# Sat, 21 Dec 2019 00:32:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 21 Dec 2019 00:32:27 GMT
RUN apk add --no-cache 		bash
# Sat, 21 Dec 2019 00:32:28 GMT
ENV NODE_ENV=production
# Sat, 21 Dec 2019 00:32:28 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 21 Dec 2019 00:33:10 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 21 Dec 2019 00:33:17 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 21 Dec 2019 00:33:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 21 Dec 2019 00:33:24 GMT
ENV GHOST_VERSION=3.2.0
# Sat, 21 Dec 2019 00:39:41 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 21 Dec 2019 00:39:44 GMT
WORKDIR /var/lib/ghost
# Sat, 21 Dec 2019 00:39:45 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 21 Dec 2019 00:39:46 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 21 Dec 2019 00:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Dec 2019 00:39:49 GMT
EXPOSE 2368
# Sat, 21 Dec 2019 00:39:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:78285f4ddf5d90a7220bed4c538bad44a42bd7cbd64898efd1cab6e592518cf0`  
		Last Modified: Fri, 20 Dec 2019 00:03:48 GMT  
		Size: 2.6 MB (2612091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d20f9ef6f345515fbfb8c36573bf0fefbd32fcac76f3b9442d3ff8ea3e3ece`  
		Last Modified: Fri, 20 Dec 2019 23:17:24 GMT  
		Size: 22.0 MB (21985952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2601ca64d702faa364dc1d329de95f1062eeff898fb34bfe134cece4b991a1`  
		Last Modified: Fri, 20 Dec 2019 23:17:15 GMT  
		Size: 1.3 MB (1327763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2051f0d4525a10a81c7e2da4b6c23d83b7b91eb1b61728814d49c85fbfa9c8`  
		Last Modified: Fri, 20 Dec 2019 23:17:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340a988586fea766fa877df2954dbaa69989c8fc266c836aa4d5c99ccc783d90`  
		Last Modified: Sat, 21 Dec 2019 00:54:35 GMT  
		Size: 9.7 KB (9727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4ca1d7f3c7c93287f101ad25d67bd97e167b167fb90e82b6f02a071d336327`  
		Last Modified: Sat, 21 Dec 2019 00:54:36 GMT  
		Size: 1.2 MB (1162910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b151dcf85dd4564edfc4c93021dd2f0c458c2100535949948262da78eb58d6a`  
		Last Modified: Sat, 21 Dec 2019 00:54:38 GMT  
		Size: 6.8 MB (6788411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c5936a24b6c053db0457f2e97f67a87231922d8f98a3aa3d68516778a4c63f`  
		Last Modified: Sat, 21 Dec 2019 00:55:04 GMT  
		Size: 69.2 MB (69247964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea45a47fa1e6ab86b61ed5f73e8bbec010fdd39039b2e6bff3183d8567f027d`  
		Last Modified: Sat, 21 Dec 2019 00:54:35 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:14e9950ec60e7eb54c2bc1eae4e1824253dc69154ca99912ef8755103dd3f033
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101570298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2cbecc23cab2324e3b1cb7f555b6a6483d9a40d09575afaff6b86895df620f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 19 Dec 2019 23:59:01 GMT
ADD file:250d98c0ca20fcc8895da5d2c1fda5ea5a2945454a9d35e350816e91dfb420b2 in / 
# Thu, 19 Dec 2019 23:59:04 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2019 21:31:49 GMT
ENV NODE_VERSION=10.18.0
# Fri, 20 Dec 2019 21:36:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Fri, 20 Dec 2019 21:36:44 GMT
ENV YARN_VERSION=1.21.1
# Fri, 20 Dec 2019 21:36:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Fri, 20 Dec 2019 21:36:49 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 20 Dec 2019 21:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2019 21:36:50 GMT
CMD ["node"]
# Sat, 21 Dec 2019 03:12:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 21 Dec 2019 03:12:57 GMT
RUN apk add --no-cache 		bash
# Sat, 21 Dec 2019 03:12:58 GMT
ENV NODE_ENV=production
# Sat, 21 Dec 2019 03:12:59 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 21 Dec 2019 03:13:26 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 21 Dec 2019 03:13:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 21 Dec 2019 03:13:29 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 21 Dec 2019 03:13:30 GMT
ENV GHOST_VERSION=3.2.0
# Sat, 21 Dec 2019 03:17:52 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 21 Dec 2019 03:17:57 GMT
WORKDIR /var/lib/ghost
# Sat, 21 Dec 2019 03:17:58 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 21 Dec 2019 03:17:58 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 21 Dec 2019 03:17:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Dec 2019 03:18:00 GMT
EXPOSE 2368
# Sat, 21 Dec 2019 03:18:01 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:425066605c7f3f988db19ea1d5d77a89b86a124d90db4f9b4ca601ee32d74c90`  
		Last Modified: Thu, 19 Dec 2019 23:59:42 GMT  
		Size: 2.4 MB (2416682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a455828bfe74aaef0e286cf5bf6f8c3a2dfa994696fb56f0a4f011b4ee6bee`  
		Last Modified: Fri, 20 Dec 2019 21:39:55 GMT  
		Size: 21.6 MB (21587887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f2335969bf1994a5cbe164c2c7b0b79dec7f65a828f1036a1b3d95e2c9ed93`  
		Last Modified: Fri, 20 Dec 2019 21:39:48 GMT  
		Size: 1.3 MB (1327755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3392cf6118f528de7c4b11341680e36bfa3af253fb770f46f893e8f24e50f8d2`  
		Last Modified: Fri, 20 Dec 2019 21:39:49 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dbc83a5d7b391a350a19567b3378f8ee60cefe42d3c294703fd0a8f5afdf48`  
		Last Modified: Sat, 21 Dec 2019 03:28:37 GMT  
		Size: 9.5 KB (9515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb3899224ec4c610cabd6d3a81823e01550c9e161a73cbebcac84813ad2398c`  
		Last Modified: Sat, 21 Dec 2019 03:28:37 GMT  
		Size: 1.1 MB (1101424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a58480c8d09c341f4796fe592c18e6184445b496c9fda93f21eb3a0ab68dbc`  
		Last Modified: Sat, 21 Dec 2019 03:28:42 GMT  
		Size: 6.8 MB (6787412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47067901b42061669880c02992848811e91177939d8ab5878ce669f4cf4af4a1`  
		Last Modified: Sat, 21 Dec 2019 03:29:04 GMT  
		Size: 68.3 MB (68338798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0087b72bfc30bbbfc1adc91d414d1322cfb2cdcad30631c7810b78a7d3ad5a`  
		Last Modified: Sat, 21 Dec 2019 03:28:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:af85d401b2e70a7e77110fa9d193d3671b547adacb32e6c3e393cf21f9c4e301
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103317258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a09176a6f48a2d2e6576c4c2e67b82cc915cad091c92a9e81613e0842828e23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2019 17:44:03 GMT
ENV NODE_VERSION=10.18.0
# Wed, 18 Dec 2019 17:50:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 18 Dec 2019 17:50:21 GMT
ENV YARN_VERSION=1.21.1
# Wed, 18 Dec 2019 17:50:32 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 18 Dec 2019 17:50:33 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 18 Dec 2019 17:50:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2019 17:50:36 GMT
CMD ["node"]
# Wed, 18 Dec 2019 18:27:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 18 Dec 2019 18:27:18 GMT
RUN apk add --no-cache 		bash
# Wed, 18 Dec 2019 18:27:18 GMT
ENV NODE_ENV=production
# Wed, 18 Dec 2019 18:27:19 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Wed, 18 Dec 2019 18:27:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 18 Dec 2019 18:27:42 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 18 Dec 2019 18:27:43 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 19 Dec 2019 01:52:21 GMT
ENV GHOST_VERSION=3.2.0
# Thu, 19 Dec 2019 02:01:11 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 19 Dec 2019 02:01:25 GMT
WORKDIR /var/lib/ghost
# Thu, 19 Dec 2019 02:01:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 19 Dec 2019 02:01:34 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 19 Dec 2019 02:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2019 02:01:52 GMT
EXPOSE 2368
# Thu, 19 Dec 2019 02:01:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe3a2f4e5d8216e33f83be1ee3cc621c627df822879ce99a65762dc665c5bc4`  
		Last Modified: Wed, 18 Dec 2019 18:03:09 GMT  
		Size: 22.6 MB (22604999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e514f58acd661f958b7a7e748fbd033a7d3d21b2cb11a0fe1599bc93e4f980ef`  
		Last Modified: Wed, 18 Dec 2019 18:02:43 GMT  
		Size: 1.3 MB (1327179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd216ec5248e34b1671e694c9fae169b7d0ce9d32a78e1e5cbd4bd74a271df7`  
		Last Modified: Wed, 18 Dec 2019 18:02:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b50e1de4f3dd3299af7c877d61dbc17922ac3e7c0e6ced6e2dfb49b6264582`  
		Last Modified: Wed, 18 Dec 2019 18:52:18 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2d557a8b7148e8d1760d98512eb44ea4e37be84afdaa15248d22440c5f2538`  
		Last Modified: Wed, 18 Dec 2019 18:52:19 GMT  
		Size: 1.2 MB (1225145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096b31901bbf1ab1e3cfa851fb5df1a3980c38a215298f8858ef4122f70c20bb`  
		Last Modified: Wed, 18 Dec 2019 18:52:19 GMT  
		Size: 6.8 MB (6787734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89971fce1d67806acd4ad12a0d66b2521756152ccfe51df8b1c1db3aff04bd0`  
		Last Modified: Thu, 19 Dec 2019 02:23:46 GMT  
		Size: 68.6 MB (68644001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0338ecf8ebd4084551cc873f8e8549000e8d7dc0c526ebdfaa0daa1a39c56a3`  
		Last Modified: Thu, 19 Dec 2019 02:23:24 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; 386

```console
$ docker pull ghost@sha256:6619dd2738d54d7cd629df041ccb6f4d92b3cb1c79bfb20049f8d7443d6be07c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103403513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636d28744a5cc4cb85a3fcc9d59b92fe89352210d85a5efb4061f414899d452a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 21 Oct 2019 16:46:04 GMT
ADD file:dd3b3676fd9c1e0983ade68242b9b9ac5c477f3e4bfc97c2e78fd5db93a441c9 in / 
# Mon, 21 Oct 2019 16:46:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2019 19:51:28 GMT
ENV NODE_VERSION=10.18.0
# Wed, 18 Dec 2019 20:19:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Wed, 18 Dec 2019 20:19:18 GMT
ENV YARN_VERSION=1.21.1
# Wed, 18 Dec 2019 20:19:21 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 18 Dec 2019 20:19:21 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 18 Dec 2019 20:19:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2019 20:19:21 GMT
CMD ["node"]
# Wed, 18 Dec 2019 20:39:19 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 18 Dec 2019 20:39:21 GMT
RUN apk add --no-cache 		bash
# Wed, 18 Dec 2019 20:39:21 GMT
ENV NODE_ENV=production
# Wed, 18 Dec 2019 20:39:21 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Wed, 18 Dec 2019 20:39:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Wed, 18 Dec 2019 20:39:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 18 Dec 2019 20:39:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 19 Dec 2019 04:02:31 GMT
ENV GHOST_VERSION=3.2.0
# Thu, 19 Dec 2019 04:07:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Thu, 19 Dec 2019 04:07:20 GMT
WORKDIR /var/lib/ghost
# Thu, 19 Dec 2019 04:07:20 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 19 Dec 2019 04:07:20 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Thu, 19 Dec 2019 04:07:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2019 04:07:21 GMT
EXPOSE 2368
# Thu, 19 Dec 2019 04:07:21 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f913bd05bf684aaa4bc173d73cfbb58abb45587962d74f0aa71df36b6b489def`  
		Last Modified: Mon, 21 Oct 2019 16:46:25 GMT  
		Size: 2.8 MB (2785939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4567cf6d84b7623433f67347038df483ce3de3c472bbc7b2a42609078e28ab05`  
		Last Modified: Wed, 18 Dec 2019 20:23:07 GMT  
		Size: 22.6 MB (22568017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae62ebb339e6fdadb786223ca7e3a694c6f6a95b8e6acd97376ebc63c89ed6d4`  
		Last Modified: Wed, 18 Dec 2019 20:23:01 GMT  
		Size: 1.3 MB (1327176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a797ab565b23f566d364e891639323b295e57040d0248b01ea9101fb4da20d`  
		Last Modified: Wed, 18 Dec 2019 20:23:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe380f3d9e0dc3df515ccf53cd059b255e7a8a651298153b5f8a086ce6a903b7`  
		Last Modified: Wed, 18 Dec 2019 20:49:35 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b697e9d376f0e714b12fd33790700db955257a520ec34382b02a49081ded5d9a`  
		Last Modified: Wed, 18 Dec 2019 20:49:36 GMT  
		Size: 1.3 MB (1259200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0246d0f541f7fe31f8fd70d4bdaa0a8c40812c5196f58305113358a860e597`  
		Last Modified: Wed, 18 Dec 2019 20:49:39 GMT  
		Size: 6.8 MB (6786983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c3364babf2ac2ef53f4940855b7c7cde48940467993d9de247310e58e6e8ee`  
		Last Modified: Thu, 19 Dec 2019 04:16:26 GMT  
		Size: 68.7 MB (68665676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b42a770d86ed35177ca04672ce7c36d1636287fa20e69839e27e317f2847b2`  
		Last Modified: Thu, 19 Dec 2019 04:16:06 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; ppc64le

```console
$ docker pull ghost@sha256:c4035e3fa2651cc6d3c417fae517f65f592a462c09b255801cedd208517d285a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108036345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16f6f3990afa588068a52be658ceab0fe9e5d53b395b7951a1897d33f8b524e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 19 Dec 2019 23:37:02 GMT
ADD file:f3e7e107e2972b4b00970eb9be40652042303a7783596a6c9cd1212a26309bc8 in / 
# Thu, 19 Dec 2019 23:37:04 GMT
CMD ["/bin/sh"]
# Fri, 20 Dec 2019 22:25:45 GMT
ENV NODE_VERSION=10.18.0
# Fri, 20 Dec 2019 22:38:02 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Fri, 20 Dec 2019 22:38:09 GMT
ENV YARN_VERSION=1.21.1
# Fri, 20 Dec 2019 22:38:19 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Fri, 20 Dec 2019 22:38:21 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Fri, 20 Dec 2019 22:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2019 22:38:28 GMT
CMD ["node"]
# Sat, 21 Dec 2019 04:19:24 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 21 Dec 2019 04:19:44 GMT
RUN apk add --no-cache 		bash
# Sat, 21 Dec 2019 04:19:48 GMT
ENV NODE_ENV=production
# Sat, 21 Dec 2019 04:19:52 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 21 Dec 2019 04:21:49 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 21 Dec 2019 04:21:56 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 21 Dec 2019 04:22:02 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 21 Dec 2019 04:22:07 GMT
ENV GHOST_VERSION=3.2.0
# Sat, 21 Dec 2019 04:29:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 21 Dec 2019 04:29:18 GMT
WORKDIR /var/lib/ghost
# Sat, 21 Dec 2019 04:29:22 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 21 Dec 2019 04:29:25 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 21 Dec 2019 04:29:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Dec 2019 04:29:29 GMT
EXPOSE 2368
# Sat, 21 Dec 2019 04:29:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cc1702756cf1ed12718b42717fddaa5c49572ef0e8f7d94ab4b77f403e335899`  
		Last Modified: Thu, 19 Dec 2019 23:37:45 GMT  
		Size: 2.8 MB (2816542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9f91a415aa7c00be789287b8cb7422189c26d488ad0da1d31b4540f70487fb`  
		Last Modified: Fri, 20 Dec 2019 22:44:04 GMT  
		Size: 24.5 MB (24532579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b13b91fd2dd5bab722d9db85edcc542c3f73c19dece939ede3f23ae251d6ae`  
		Last Modified: Fri, 20 Dec 2019 22:43:57 GMT  
		Size: 1.3 MB (1327768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83574a9c5605730fc69ae2ed5aaa6693ae8b78ea3974fd1da55d88d0ed167c7d`  
		Last Modified: Fri, 20 Dec 2019 22:43:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2e12a2f1032a950120b37f1308898129a1f336c3caa5b584d7c47818e22e02`  
		Last Modified: Sat, 21 Dec 2019 04:44:04 GMT  
		Size: 10.4 KB (10402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0465222e0e01f3e2fb669ee033bf4cee7b5a685e0b594d4375145c03a33e90`  
		Last Modified: Sat, 21 Dec 2019 04:44:09 GMT  
		Size: 1.3 MB (1293080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a3e308650c5597e957eae129064bbaa78cbfc9904f9a638a5d16747319ec32`  
		Last Modified: Sat, 21 Dec 2019 04:44:22 GMT  
		Size: 6.8 MB (6788377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074664938c7244455de25e2f32289df87ff5b27f79508a4dcb746dc7416fd61a`  
		Last Modified: Sat, 21 Dec 2019 04:45:14 GMT  
		Size: 71.3 MB (71266771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1139b93b3fd2ca6ca01611874820b255591ec157f3c1af8c99dfe780506aff10`  
		Last Modified: Sat, 21 Dec 2019 04:44:04 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:3-alpine` - linux; s390x

```console
$ docker pull ghost@sha256:dcdb7594b2ba0796255b7d12601211865f4e0aeb89be23cf2468f3463155af00
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103929847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6845d389ec5bcd15abfdc4ddf47910b57ee78481d569cf440173050037fc748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 19 Dec 2019 23:41:47 GMT
ADD file:76b98628dfe42e69b2ce24e40f1d584b0245c65db7fd20160787dba84f6d01fc in / 
# Thu, 19 Dec 2019 23:41:47 GMT
CMD ["/bin/sh"]
# Sat, 21 Dec 2019 02:59:51 GMT
ENV NODE_VERSION=10.18.0
# Sat, 21 Dec 2019 03:10:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="043f9e1c412a391f42a9667373b851590a9a77c08cf6fde6828a3cdb3fb8f316"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps
# Sat, 21 Dec 2019 03:10:46 GMT
ENV YARN_VERSION=1.21.1
# Sat, 21 Dec 2019 03:10:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Sat, 21 Dec 2019 03:10:48 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 21 Dec 2019 03:10:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Dec 2019 03:10:49 GMT
CMD ["node"]
# Sat, 21 Dec 2019 03:46:32 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 21 Dec 2019 03:46:33 GMT
RUN apk add --no-cache 		bash
# Sat, 21 Dec 2019 03:46:33 GMT
ENV NODE_ENV=production
# Sat, 21 Dec 2019 03:46:34 GMT
ENV GHOST_CLI_VERSION=1.13.1
# Sat, 21 Dec 2019 03:46:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Sat, 21 Dec 2019 03:46:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 21 Dec 2019 03:46:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 21 Dec 2019 03:46:45 GMT
ENV GHOST_VERSION=3.2.0
# Sat, 21 Dec 2019 03:48:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! su-exec node yarn add "sqlite3@$sqlite3Version" --force; then 		apk add --no-cache --virtual .build-deps python make gcc g++ libc-dev; 				su-exec node yarn add "sqlite3@$sqlite3Version" --force --build-from-source; 				apk del --no-network .build-deps; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Sat, 21 Dec 2019 03:48:27 GMT
WORKDIR /var/lib/ghost
# Sat, 21 Dec 2019 03:48:27 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 21 Dec 2019 03:48:27 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Sat, 21 Dec 2019 03:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Dec 2019 03:48:27 GMT
EXPOSE 2368
# Sat, 21 Dec 2019 03:48:28 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cde57aed53ae0e310089f2638677af1321dcf6e45d514b758c1f637f1a2d2f9b`  
		Last Modified: Thu, 19 Dec 2019 23:42:27 GMT  
		Size: 2.6 MB (2579533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8195a750757a3823665cb4d8d777c2aacfba61c8f0da162c2b80d6e4ccf956e2`  
		Last Modified: Sat, 21 Dec 2019 03:12:45 GMT  
		Size: 22.6 MB (22597220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa825cbdb6734049555d77da59003c2bd8f09c5e50ce354f25ab0069380fa32`  
		Last Modified: Sat, 21 Dec 2019 03:12:39 GMT  
		Size: 1.3 MB (1327738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06c2f61f00e79e8cac2aee607ed4659a6ba5b5c2ef1460ad7eb564d4a55c7ad`  
		Last Modified: Sat, 21 Dec 2019 03:12:39 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f332acea150de72eed64de301b328355adf210e2e1fff0b63208a00bc4bedf5e`  
		Last Modified: Sat, 21 Dec 2019 03:52:39 GMT  
		Size: 10.0 KB (9992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8910400ad2f4e633d489d5de2e881da3e39c1ef52cbb0fe9f3717aa896008bc`  
		Last Modified: Sat, 21 Dec 2019 03:52:39 GMT  
		Size: 1.2 MB (1245135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae649cdc97325ac9598d3d400ca430b2da8b8917b39b6aff7e3bc721eb855c5`  
		Last Modified: Sat, 21 Dec 2019 03:52:40 GMT  
		Size: 6.8 MB (6787374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9bf8f11c0ca13087d1666e051cf75540dfb09a90b74573d0d19b3ad2ee8532`  
		Last Modified: Sat, 21 Dec 2019 03:52:48 GMT  
		Size: 69.4 MB (69382031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c59d63fe98442bca286be2a2fa6038f3223f0c9f2e37799b9fa5490c0f3ed2`  
		Last Modified: Sat, 21 Dec 2019 03:52:38 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
