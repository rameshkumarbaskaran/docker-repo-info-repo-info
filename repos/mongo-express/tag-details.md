<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo-express`

-	[`mongo-express:0.54`](#mongo-express054)
-	[`mongo-express:0.54.0`](#mongo-express0540)
-	[`mongo-express:1.0.0-alpha`](#mongo-express100-alpha)
-	[`mongo-express:1.0.0-alpha.4`](#mongo-express100-alpha4)
-	[`mongo-express:latest`](#mongo-expresslatest)

## `mongo-express:0.54`

```console
$ docker pull mongo-express@sha256:f8ea7bad54a7535ad2a7b42ea3372a520787e4ceefaeb4811f6553e5c33086e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:0.54` - linux; amd64

```console
$ docker pull mongo-express@sha256:2b22d48f32f643785cf505983d4534d009879a781518028d193eb001ca7de16b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46739693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a26fe5313924a0f72b951e492db84540b84ff6b618048bb150b98c8095f0275`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 17:27:35 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 17:27:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 17:27:42 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 17:27:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 17:27:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:27:46 GMT
CMD ["node"]
# Wed, 07 Jul 2021 17:58:01 GMT
RUN apk add --no-cache bash tini
# Wed, 07 Jul 2021 17:58:02 GMT
EXPOSE 8081
# Wed, 07 Jul 2021 17:58:22 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Wed, 07 Jul 2021 17:58:22 GMT
ENV MONGO_EXPRESS=0.54.0
# Wed, 07 Jul 2021 17:58:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Wed, 07 Jul 2021 17:58:38 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Wed, 07 Jul 2021 17:58:38 GMT
WORKDIR /node_modules/mongo-express
# Wed, 07 Jul 2021 17:58:39 GMT
RUN cp config.default.js config.js
# Wed, 07 Jul 2021 17:58:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:58:40 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb195d94de45050928c69d40bf7912137c9e99b24a8d50de74451be24bc89fe`  
		Last Modified: Wed, 07 Jul 2021 17:40:07 GMT  
		Size: 24.6 MB (24601007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b379f7fa3622fff221bc37f0138ad0e2f62f4b112940a8d9c3dacafa646dd`  
		Last Modified: Wed, 07 Jul 2021 17:40:02 GMT  
		Size: 2.2 MB (2239448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a9bc999d9d6e93526e2c11dff4ce0d2636868002ac9f09de3a1b8183b4829`  
		Last Modified: Wed, 07 Jul 2021 17:40:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ef2ef6331a2e6ab55f4ddced7a843d8d2bdb549cff2e36569e6dedb827bdb3`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 789.3 KB (789318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21539eed3d1fadffadf807786b5cb959119a90248b3baf4480b0e62f222bdb1`  
		Last Modified: Wed, 07 Jul 2021 17:59:12 GMT  
		Size: 16.3 MB (16289590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd4c0f594aab55e1f6fd099f3c60c13e8b4450874d893f22ce27747daed4a65`  
		Last Modified: Wed, 07 Jul 2021 17:59:10 GMT  
		Size: 656.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bee199d35375a48a4fa1d308348bbcde070a496a52a82bbd24250188922c44`  
		Last Modified: Wed, 07 Jul 2021 17:59:10 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:0.54` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:c3141d99713db021901d5638989c8a5b73333cc2f7551b6c7e9fc628b454fb3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46849703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f0eedacc473958a2ea8b29a1c61ee0925bacebeefd37ef7c8e4ecccc59d436`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 21:56:32 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 22:24:04 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 22:24:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 22:24:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 22:24:08 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 22:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 22:24:09 GMT
CMD ["node"]
# Thu, 08 Jul 2021 00:43:09 GMT
RUN apk add --no-cache bash tini
# Thu, 08 Jul 2021 00:43:09 GMT
EXPOSE 8081
# Thu, 08 Jul 2021 00:43:34 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 08 Jul 2021 00:43:34 GMT
ENV MONGO_EXPRESS=0.54.0
# Thu, 08 Jul 2021 00:43:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 08 Jul 2021 00:43:51 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Thu, 08 Jul 2021 00:43:51 GMT
WORKDIR /node_modules/mongo-express
# Thu, 08 Jul 2021 00:43:52 GMT
RUN cp config.default.js config.js
# Thu, 08 Jul 2021 00:43:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 08 Jul 2021 00:43:52 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a2c32409956f0c58ce27fa21274380f2636d4ee7ac161bc694ff6023868540`  
		Last Modified: Wed, 07 Jul 2021 23:08:10 GMT  
		Size: 24.7 MB (24729045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f79c6c79c2b576b3522c7d1cc21960b9235f115671c9fc43e3780450f35531`  
		Last Modified: Wed, 07 Jul 2021 23:08:06 GMT  
		Size: 2.3 MB (2299277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096c54f41569435125695b6ab6a5529e489ac10f201100facb9a9be11114cf92`  
		Last Modified: Wed, 07 Jul 2021 23:08:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9179555d6aac60ce2c92786177307ef58ed27c58970100e1a06d0d15b83961`  
		Last Modified: Thu, 08 Jul 2021 00:44:12 GMT  
		Size: 800.1 KB (800073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3d589dd5f39362900454641db6f302ac489e2ce333f94affe012a06bc33b6d`  
		Last Modified: Thu, 08 Jul 2021 00:44:33 GMT  
		Size: 16.3 MB (16290296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bef215c03a2f0d9023e74606c6a9b951a2f97d50b77ab279656566bc97b357`  
		Last Modified: Thu, 08 Jul 2021 00:44:31 GMT  
		Size: 655.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd9c64762bea68aea9b4a915c18ae1a42be36f274132df7d0bf011e0489afd1`  
		Last Modified: Thu, 08 Jul 2021 00:44:31 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:0.54.0`

```console
$ docker pull mongo-express@sha256:f8ea7bad54a7535ad2a7b42ea3372a520787e4ceefaeb4811f6553e5c33086e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:0.54.0` - linux; amd64

```console
$ docker pull mongo-express@sha256:2b22d48f32f643785cf505983d4534d009879a781518028d193eb001ca7de16b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46739693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a26fe5313924a0f72b951e492db84540b84ff6b618048bb150b98c8095f0275`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 17:27:35 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 17:27:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 17:27:42 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 17:27:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 17:27:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:27:46 GMT
CMD ["node"]
# Wed, 07 Jul 2021 17:58:01 GMT
RUN apk add --no-cache bash tini
# Wed, 07 Jul 2021 17:58:02 GMT
EXPOSE 8081
# Wed, 07 Jul 2021 17:58:22 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Wed, 07 Jul 2021 17:58:22 GMT
ENV MONGO_EXPRESS=0.54.0
# Wed, 07 Jul 2021 17:58:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Wed, 07 Jul 2021 17:58:38 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Wed, 07 Jul 2021 17:58:38 GMT
WORKDIR /node_modules/mongo-express
# Wed, 07 Jul 2021 17:58:39 GMT
RUN cp config.default.js config.js
# Wed, 07 Jul 2021 17:58:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:58:40 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb195d94de45050928c69d40bf7912137c9e99b24a8d50de74451be24bc89fe`  
		Last Modified: Wed, 07 Jul 2021 17:40:07 GMT  
		Size: 24.6 MB (24601007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b379f7fa3622fff221bc37f0138ad0e2f62f4b112940a8d9c3dacafa646dd`  
		Last Modified: Wed, 07 Jul 2021 17:40:02 GMT  
		Size: 2.2 MB (2239448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a9bc999d9d6e93526e2c11dff4ce0d2636868002ac9f09de3a1b8183b4829`  
		Last Modified: Wed, 07 Jul 2021 17:40:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ef2ef6331a2e6ab55f4ddced7a843d8d2bdb549cff2e36569e6dedb827bdb3`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 789.3 KB (789318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21539eed3d1fadffadf807786b5cb959119a90248b3baf4480b0e62f222bdb1`  
		Last Modified: Wed, 07 Jul 2021 17:59:12 GMT  
		Size: 16.3 MB (16289590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd4c0f594aab55e1f6fd099f3c60c13e8b4450874d893f22ce27747daed4a65`  
		Last Modified: Wed, 07 Jul 2021 17:59:10 GMT  
		Size: 656.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bee199d35375a48a4fa1d308348bbcde070a496a52a82bbd24250188922c44`  
		Last Modified: Wed, 07 Jul 2021 17:59:10 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:0.54.0` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:c3141d99713db021901d5638989c8a5b73333cc2f7551b6c7e9fc628b454fb3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46849703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f0eedacc473958a2ea8b29a1c61ee0925bacebeefd37ef7c8e4ecccc59d436`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 21:56:32 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 22:24:04 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 22:24:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 22:24:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 22:24:08 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 22:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 22:24:09 GMT
CMD ["node"]
# Thu, 08 Jul 2021 00:43:09 GMT
RUN apk add --no-cache bash tini
# Thu, 08 Jul 2021 00:43:09 GMT
EXPOSE 8081
# Thu, 08 Jul 2021 00:43:34 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 08 Jul 2021 00:43:34 GMT
ENV MONGO_EXPRESS=0.54.0
# Thu, 08 Jul 2021 00:43:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 08 Jul 2021 00:43:51 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Thu, 08 Jul 2021 00:43:51 GMT
WORKDIR /node_modules/mongo-express
# Thu, 08 Jul 2021 00:43:52 GMT
RUN cp config.default.js config.js
# Thu, 08 Jul 2021 00:43:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 08 Jul 2021 00:43:52 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a2c32409956f0c58ce27fa21274380f2636d4ee7ac161bc694ff6023868540`  
		Last Modified: Wed, 07 Jul 2021 23:08:10 GMT  
		Size: 24.7 MB (24729045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f79c6c79c2b576b3522c7d1cc21960b9235f115671c9fc43e3780450f35531`  
		Last Modified: Wed, 07 Jul 2021 23:08:06 GMT  
		Size: 2.3 MB (2299277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096c54f41569435125695b6ab6a5529e489ac10f201100facb9a9be11114cf92`  
		Last Modified: Wed, 07 Jul 2021 23:08:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9179555d6aac60ce2c92786177307ef58ed27c58970100e1a06d0d15b83961`  
		Last Modified: Thu, 08 Jul 2021 00:44:12 GMT  
		Size: 800.1 KB (800073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3d589dd5f39362900454641db6f302ac489e2ce333f94affe012a06bc33b6d`  
		Last Modified: Thu, 08 Jul 2021 00:44:33 GMT  
		Size: 16.3 MB (16290296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bef215c03a2f0d9023e74606c6a9b951a2f97d50b77ab279656566bc97b357`  
		Last Modified: Thu, 08 Jul 2021 00:44:31 GMT  
		Size: 655.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd9c64762bea68aea9b4a915c18ae1a42be36f274132df7d0bf011e0489afd1`  
		Last Modified: Thu, 08 Jul 2021 00:44:31 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.0-alpha`

```console
$ docker pull mongo-express@sha256:83314d59ee5c7ad2499357b24736f80066e80373267deea8e9ed81a2a9a5c978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.0-alpha` - linux; amd64

```console
$ docker pull mongo-express@sha256:7492a23cbf0c6c146bc6feebae5ff6c917d9d3513058174b08b2763c486cd156
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49475143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fe1b7702e7d84a16efcd291f27e1d5961ce571963f5ffa16d7026b8f88715d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 17:27:35 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 17:27:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 17:27:42 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 17:27:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 17:27:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:27:46 GMT
CMD ["node"]
# Wed, 07 Jul 2021 17:58:01 GMT
RUN apk add --no-cache bash tini
# Wed, 07 Jul 2021 17:58:02 GMT
EXPOSE 8081
# Wed, 07 Jul 2021 17:58:02 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Wed, 07 Jul 2021 17:58:02 GMT
ENV MONGO_EXPRESS=1.0.0-alpha.4
# Wed, 07 Jul 2021 17:58:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Wed, 07 Jul 2021 17:58:17 GMT
COPY file:4835df10525ec6f18e6339ce0c331b087391dd3279d964040c96a41ba7bf90b7 in / 
# Wed, 07 Jul 2021 17:58:18 GMT
WORKDIR /node_modules/mongo-express
# Wed, 07 Jul 2021 17:58:19 GMT
RUN cp config.default.js config.js
# Wed, 07 Jul 2021 17:58:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:58:19 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb195d94de45050928c69d40bf7912137c9e99b24a8d50de74451be24bc89fe`  
		Last Modified: Wed, 07 Jul 2021 17:40:07 GMT  
		Size: 24.6 MB (24601007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b379f7fa3622fff221bc37f0138ad0e2f62f4b112940a8d9c3dacafa646dd`  
		Last Modified: Wed, 07 Jul 2021 17:40:02 GMT  
		Size: 2.2 MB (2239448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a9bc999d9d6e93526e2c11dff4ce0d2636868002ac9f09de3a1b8183b4829`  
		Last Modified: Wed, 07 Jul 2021 17:40:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ef2ef6331a2e6ab55f4ddced7a843d8d2bdb549cff2e36569e6dedb827bdb3`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 789.3 KB (789318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257207a2d6877dbe2dc7292a2c0e5e5d133d88d2a3deab61c9ddf02eadc76626`  
		Last Modified: Wed, 07 Jul 2021 17:58:57 GMT  
		Size: 19.0 MB (19024811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5edc3885b40a3809041db1a4a558532a0d71611cecf043ac1a796a9325a4b9`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9279adbd02a16e2530c9b84b6f09a2ca5dcce94b9ff85bb2bed2ada691cbb`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.0-alpha` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:67a3e6f122622439ad72a648bf85b7b9a43e8bf5bc9bd3e3db8e4907eac7c470
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49586661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c514aa936f6cec46a8b16553c17c75453b816b82c8b91a407630b3f4441907`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 21:56:32 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 22:24:04 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 22:24:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 22:24:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 22:24:08 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 22:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 22:24:09 GMT
CMD ["node"]
# Thu, 08 Jul 2021 00:43:09 GMT
RUN apk add --no-cache bash tini
# Thu, 08 Jul 2021 00:43:09 GMT
EXPOSE 8081
# Thu, 08 Jul 2021 00:43:09 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 08 Jul 2021 00:43:09 GMT
ENV MONGO_EXPRESS=1.0.0-alpha.4
# Thu, 08 Jul 2021 00:43:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 08 Jul 2021 00:43:26 GMT
COPY file:4835df10525ec6f18e6339ce0c331b087391dd3279d964040c96a41ba7bf90b7 in / 
# Thu, 08 Jul 2021 00:43:26 GMT
WORKDIR /node_modules/mongo-express
# Thu, 08 Jul 2021 00:43:27 GMT
RUN cp config.default.js config.js
# Thu, 08 Jul 2021 00:43:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 08 Jul 2021 00:43:27 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a2c32409956f0c58ce27fa21274380f2636d4ee7ac161bc694ff6023868540`  
		Last Modified: Wed, 07 Jul 2021 23:08:10 GMT  
		Size: 24.7 MB (24729045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f79c6c79c2b576b3522c7d1cc21960b9235f115671c9fc43e3780450f35531`  
		Last Modified: Wed, 07 Jul 2021 23:08:06 GMT  
		Size: 2.3 MB (2299277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096c54f41569435125695b6ab6a5529e489ac10f201100facb9a9be11114cf92`  
		Last Modified: Wed, 07 Jul 2021 23:08:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9179555d6aac60ce2c92786177307ef58ed27c58970100e1a06d0d15b83961`  
		Last Modified: Thu, 08 Jul 2021 00:44:12 GMT  
		Size: 800.1 KB (800073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f22b7c6e0c4307dde30c4d27aeff698b712b5765ead8fcc3ebadaf4874445`  
		Last Modified: Thu, 08 Jul 2021 00:44:15 GMT  
		Size: 19.0 MB (19027026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da37d1897c7519717731d9bf0448c866e8b8fdbfd7eccee2d4b5237299b7564a`  
		Last Modified: Thu, 08 Jul 2021 00:44:12 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d94ade431db776ce37b6d758bb0e763cbdb6833bd069b973d9009476e3907cb`  
		Last Modified: Thu, 08 Jul 2021 00:44:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.0-alpha.4`

```console
$ docker pull mongo-express@sha256:83314d59ee5c7ad2499357b24736f80066e80373267deea8e9ed81a2a9a5c978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.0-alpha.4` - linux; amd64

```console
$ docker pull mongo-express@sha256:7492a23cbf0c6c146bc6feebae5ff6c917d9d3513058174b08b2763c486cd156
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49475143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fe1b7702e7d84a16efcd291f27e1d5961ce571963f5ffa16d7026b8f88715d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 17:27:35 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 17:27:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 17:27:42 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 17:27:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 17:27:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:27:46 GMT
CMD ["node"]
# Wed, 07 Jul 2021 17:58:01 GMT
RUN apk add --no-cache bash tini
# Wed, 07 Jul 2021 17:58:02 GMT
EXPOSE 8081
# Wed, 07 Jul 2021 17:58:02 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Wed, 07 Jul 2021 17:58:02 GMT
ENV MONGO_EXPRESS=1.0.0-alpha.4
# Wed, 07 Jul 2021 17:58:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Wed, 07 Jul 2021 17:58:17 GMT
COPY file:4835df10525ec6f18e6339ce0c331b087391dd3279d964040c96a41ba7bf90b7 in / 
# Wed, 07 Jul 2021 17:58:18 GMT
WORKDIR /node_modules/mongo-express
# Wed, 07 Jul 2021 17:58:19 GMT
RUN cp config.default.js config.js
# Wed, 07 Jul 2021 17:58:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:58:19 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb195d94de45050928c69d40bf7912137c9e99b24a8d50de74451be24bc89fe`  
		Last Modified: Wed, 07 Jul 2021 17:40:07 GMT  
		Size: 24.6 MB (24601007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b379f7fa3622fff221bc37f0138ad0e2f62f4b112940a8d9c3dacafa646dd`  
		Last Modified: Wed, 07 Jul 2021 17:40:02 GMT  
		Size: 2.2 MB (2239448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a9bc999d9d6e93526e2c11dff4ce0d2636868002ac9f09de3a1b8183b4829`  
		Last Modified: Wed, 07 Jul 2021 17:40:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ef2ef6331a2e6ab55f4ddced7a843d8d2bdb549cff2e36569e6dedb827bdb3`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 789.3 KB (789318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257207a2d6877dbe2dc7292a2c0e5e5d133d88d2a3deab61c9ddf02eadc76626`  
		Last Modified: Wed, 07 Jul 2021 17:58:57 GMT  
		Size: 19.0 MB (19024811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5edc3885b40a3809041db1a4a558532a0d71611cecf043ac1a796a9325a4b9`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9279adbd02a16e2530c9b84b6f09a2ca5dcce94b9ff85bb2bed2ada691cbb`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.0-alpha.4` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:67a3e6f122622439ad72a648bf85b7b9a43e8bf5bc9bd3e3db8e4907eac7c470
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49586661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c514aa936f6cec46a8b16553c17c75453b816b82c8b91a407630b3f4441907`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 21:56:32 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 22:24:04 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 22:24:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 22:24:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 22:24:08 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 22:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 22:24:09 GMT
CMD ["node"]
# Thu, 08 Jul 2021 00:43:09 GMT
RUN apk add --no-cache bash tini
# Thu, 08 Jul 2021 00:43:09 GMT
EXPOSE 8081
# Thu, 08 Jul 2021 00:43:09 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 08 Jul 2021 00:43:09 GMT
ENV MONGO_EXPRESS=1.0.0-alpha.4
# Thu, 08 Jul 2021 00:43:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 08 Jul 2021 00:43:26 GMT
COPY file:4835df10525ec6f18e6339ce0c331b087391dd3279d964040c96a41ba7bf90b7 in / 
# Thu, 08 Jul 2021 00:43:26 GMT
WORKDIR /node_modules/mongo-express
# Thu, 08 Jul 2021 00:43:27 GMT
RUN cp config.default.js config.js
# Thu, 08 Jul 2021 00:43:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 08 Jul 2021 00:43:27 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a2c32409956f0c58ce27fa21274380f2636d4ee7ac161bc694ff6023868540`  
		Last Modified: Wed, 07 Jul 2021 23:08:10 GMT  
		Size: 24.7 MB (24729045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f79c6c79c2b576b3522c7d1cc21960b9235f115671c9fc43e3780450f35531`  
		Last Modified: Wed, 07 Jul 2021 23:08:06 GMT  
		Size: 2.3 MB (2299277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096c54f41569435125695b6ab6a5529e489ac10f201100facb9a9be11114cf92`  
		Last Modified: Wed, 07 Jul 2021 23:08:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9179555d6aac60ce2c92786177307ef58ed27c58970100e1a06d0d15b83961`  
		Last Modified: Thu, 08 Jul 2021 00:44:12 GMT  
		Size: 800.1 KB (800073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f22b7c6e0c4307dde30c4d27aeff698b712b5765ead8fcc3ebadaf4874445`  
		Last Modified: Thu, 08 Jul 2021 00:44:15 GMT  
		Size: 19.0 MB (19027026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da37d1897c7519717731d9bf0448c866e8b8fdbfd7eccee2d4b5237299b7564a`  
		Last Modified: Thu, 08 Jul 2021 00:44:12 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d94ade431db776ce37b6d758bb0e763cbdb6833bd069b973d9009476e3907cb`  
		Last Modified: Thu, 08 Jul 2021 00:44:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:latest`

```console
$ docker pull mongo-express@sha256:83314d59ee5c7ad2499357b24736f80066e80373267deea8e9ed81a2a9a5c978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:latest` - linux; amd64

```console
$ docker pull mongo-express@sha256:7492a23cbf0c6c146bc6feebae5ff6c917d9d3513058174b08b2763c486cd156
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49475143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fe1b7702e7d84a16efcd291f27e1d5961ce571963f5ffa16d7026b8f88715d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 17:27:35 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 17:27:41 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 17:27:42 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 17:27:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 17:27:46 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 17:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:27:46 GMT
CMD ["node"]
# Wed, 07 Jul 2021 17:58:01 GMT
RUN apk add --no-cache bash tini
# Wed, 07 Jul 2021 17:58:02 GMT
EXPOSE 8081
# Wed, 07 Jul 2021 17:58:02 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Wed, 07 Jul 2021 17:58:02 GMT
ENV MONGO_EXPRESS=1.0.0-alpha.4
# Wed, 07 Jul 2021 17:58:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Wed, 07 Jul 2021 17:58:17 GMT
COPY file:4835df10525ec6f18e6339ce0c331b087391dd3279d964040c96a41ba7bf90b7 in / 
# Wed, 07 Jul 2021 17:58:18 GMT
WORKDIR /node_modules/mongo-express
# Wed, 07 Jul 2021 17:58:19 GMT
RUN cp config.default.js config.js
# Wed, 07 Jul 2021 17:58:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 07 Jul 2021 17:58:19 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb195d94de45050928c69d40bf7912137c9e99b24a8d50de74451be24bc89fe`  
		Last Modified: Wed, 07 Jul 2021 17:40:07 GMT  
		Size: 24.6 MB (24601007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b379f7fa3622fff221bc37f0138ad0e2f62f4b112940a8d9c3dacafa646dd`  
		Last Modified: Wed, 07 Jul 2021 17:40:02 GMT  
		Size: 2.2 MB (2239448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8a9bc999d9d6e93526e2c11dff4ce0d2636868002ac9f09de3a1b8183b4829`  
		Last Modified: Wed, 07 Jul 2021 17:40:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ef2ef6331a2e6ab55f4ddced7a843d8d2bdb549cff2e36569e6dedb827bdb3`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 789.3 KB (789318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257207a2d6877dbe2dc7292a2c0e5e5d133d88d2a3deab61c9ddf02eadc76626`  
		Last Modified: Wed, 07 Jul 2021 17:58:57 GMT  
		Size: 19.0 MB (19024811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5edc3885b40a3809041db1a4a558532a0d71611cecf043ac1a796a9325a4b9`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9279adbd02a16e2530c9b84b6f09a2ca5dcce94b9ff85bb2bed2ada691cbb`  
		Last Modified: Wed, 07 Jul 2021 17:58:54 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:latest` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:67a3e6f122622439ad72a648bf85b7b9a43e8bf5bc9bd3e3db8e4907eac7c470
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49586661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c514aa936f6cec46a8b16553c17c75453b816b82c8b91a407630b3f4441907`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 21:56:32 GMT
ENV NODE_VERSION=12.22.3
# Wed, 07 Jul 2021 22:24:04 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="8ed8e250b923427519fb15e2c451663c901d858388b644e1da58f55f878b361c"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python2     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       74F12602B6F1C4E913FAA37AD3A89613643B6201       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       A48C2BEE680E841632CD4E44F07496B3EB3C1762       108F52B48DB57BB0CC439B2997B01419BD92F80A       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Wed, 07 Jul 2021 22:24:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 07 Jul 2021 22:24:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 07 Jul 2021 22:24:08 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 07 Jul 2021 22:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 22:24:09 GMT
CMD ["node"]
# Thu, 08 Jul 2021 00:43:09 GMT
RUN apk add --no-cache bash tini
# Thu, 08 Jul 2021 00:43:09 GMT
EXPOSE 8081
# Thu, 08 Jul 2021 00:43:09 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 08 Jul 2021 00:43:09 GMT
ENV MONGO_EXPRESS=1.0.0-alpha.4
# Thu, 08 Jul 2021 00:43:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 08 Jul 2021 00:43:26 GMT
COPY file:4835df10525ec6f18e6339ce0c331b087391dd3279d964040c96a41ba7bf90b7 in / 
# Thu, 08 Jul 2021 00:43:26 GMT
WORKDIR /node_modules/mongo-express
# Thu, 08 Jul 2021 00:43:27 GMT
RUN cp config.default.js config.js
# Thu, 08 Jul 2021 00:43:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 08 Jul 2021 00:43:27 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a2c32409956f0c58ce27fa21274380f2636d4ee7ac161bc694ff6023868540`  
		Last Modified: Wed, 07 Jul 2021 23:08:10 GMT  
		Size: 24.7 MB (24729045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f79c6c79c2b576b3522c7d1cc21960b9235f115671c9fc43e3780450f35531`  
		Last Modified: Wed, 07 Jul 2021 23:08:06 GMT  
		Size: 2.3 MB (2299277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096c54f41569435125695b6ab6a5529e489ac10f201100facb9a9be11114cf92`  
		Last Modified: Wed, 07 Jul 2021 23:08:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9179555d6aac60ce2c92786177307ef58ed27c58970100e1a06d0d15b83961`  
		Last Modified: Thu, 08 Jul 2021 00:44:12 GMT  
		Size: 800.1 KB (800073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f22b7c6e0c4307dde30c4d27aeff698b712b5765ead8fcc3ebadaf4874445`  
		Last Modified: Thu, 08 Jul 2021 00:44:15 GMT  
		Size: 19.0 MB (19027026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da37d1897c7519717731d9bf0448c866e8b8fdbfd7eccee2d4b5237299b7564a`  
		Last Modified: Thu, 08 Jul 2021 00:44:12 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d94ade431db776ce37b6d758bb0e763cbdb6833bd069b973d9009476e3907cb`  
		Last Modified: Thu, 08 Jul 2021 00:44:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
