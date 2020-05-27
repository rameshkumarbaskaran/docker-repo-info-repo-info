<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo-express`

-	[`mongo-express:0.54`](#mongo-express054)
-	[`mongo-express:0.54.0`](#mongo-express0540)
-	[`mongo-express:latest`](#mongo-expresslatest)

## `mongo-express:0.54`

```console
$ docker pull mongo-express@sha256:bef1da1e94ac497e2016429a4b9521e038fd0590f10c3853f4f6e69b8e1f8ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:0.54` - linux; amd64

```console
$ docker pull mongo-express@sha256:ee184818d2f005f223678830f0f8e1d09541fe33817c0580b6191135571477e7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47221155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae0a154c4d73f1e61a532148942c582fbfad22944638d4307a4710daa1398b6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2020 22:45:00 GMT
ENV NODE_VERSION=12.17.0
# Tue, 26 May 2020 22:45:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="fbd8916cc5a3c85dc503cc1fe9606cf8860152c4e8b2f2fcc729e48db3e3d654"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 26 May 2020 22:45:06 GMT
ENV YARN_VERSION=1.22.4
# Tue, 26 May 2020 22:45:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 26 May 2020 22:45:08 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 26 May 2020 22:45:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2020 22:45:09 GMT
CMD ["node"]
# Tue, 26 May 2020 23:04:16 GMT
RUN apk add --no-cache bash tini
# Tue, 26 May 2020 23:04:17 GMT
EXPOSE 8081
# Tue, 26 May 2020 23:04:17 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Tue, 26 May 2020 23:04:17 GMT
ENV MONGO_EXPRESS=0.54.0
# Tue, 26 May 2020 23:04:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Tue, 26 May 2020 23:04:50 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Tue, 26 May 2020 23:04:51 GMT
WORKDIR /node_modules/mongo-express
# Tue, 26 May 2020 23:04:52 GMT
RUN cp config.default.js config.js
# Tue, 26 May 2020 23:04:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2020 23:04:53 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2258f794beb1f503eb2951ce0825088dfaf1b1351cec61d423a9d36e6074ced`  
		Last Modified: Tue, 26 May 2020 22:48:30 GMT  
		Size: 24.7 MB (24740785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb2c1711f4234fb4ece973e4c6a76c536ea07629e4e1fe72d6e5f9def0100e`  
		Last Modified: Tue, 26 May 2020 22:48:23 GMT  
		Size: 2.2 MB (2239066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c89d818d1fec3df1d4a708492894de475c4daa5f8053a4d589d9b0484e2c099`  
		Last Modified: Tue, 26 May 2020 22:48:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98464beaa01d5bd3c3a3c5cc4bbed22fd85acf27795c921e4ac111bca94defbc`  
		Last Modified: Tue, 26 May 2020 23:05:08 GMT  
		Size: 789.2 KB (789191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46034b648892c97835f4629fee327f4d4080ac3632f797dbac7d2d6bda0064a`  
		Last Modified: Tue, 26 May 2020 23:05:12 GMT  
		Size: 16.6 MB (16634712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b1fb5cba44f347581ac773ce0354b354204635e5eee97d842e0e45525214fd`  
		Last Modified: Tue, 26 May 2020 23:05:06 GMT  
		Size: 655.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6590f2ff35b683538683ce843fe70b89d35fb04ee61aca34eb446213c0ca4eec`  
		Last Modified: Tue, 26 May 2020 23:05:06 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:0.54` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:d2c56758de742920482281e3a1949abcf2287e8f5226fb610d066e1a99c32036
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b30afdc3f8e4dfbda3f4a5f17dcfb432c21b8eb6741ff0dd235c5b11a5f9ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2020 22:31:07 GMT
ENV NODE_VERSION=12.17.0
# Tue, 26 May 2020 22:42:13 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="fbd8916cc5a3c85dc503cc1fe9606cf8860152c4e8b2f2fcc729e48db3e3d654"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 26 May 2020 22:42:16 GMT
ENV YARN_VERSION=1.22.4
# Tue, 26 May 2020 22:42:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 26 May 2020 22:42:28 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 26 May 2020 22:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2020 22:42:32 GMT
CMD ["node"]
# Tue, 26 May 2020 23:32:53 GMT
RUN apk add --no-cache bash tini
# Tue, 26 May 2020 23:32:56 GMT
EXPOSE 8081
# Tue, 26 May 2020 23:32:58 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Tue, 26 May 2020 23:33:00 GMT
ENV MONGO_EXPRESS=0.54.0
# Tue, 26 May 2020 23:33:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Tue, 26 May 2020 23:33:48 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Tue, 26 May 2020 23:33:50 GMT
WORKDIR /node_modules/mongo-express
# Tue, 26 May 2020 23:33:57 GMT
RUN cp config.default.js config.js
# Tue, 26 May 2020 23:33:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2020 23:33:59 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0645aba79184b4b2f8746b951cd4f319eaad9894739aa71726e80e7454bd7a`  
		Last Modified: Tue, 26 May 2020 22:49:44 GMT  
		Size: 24.9 MB (24864671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf79fc3473c4e5879fc6ec74fda103961b7e6a2c89dd7e21c06085e40ee2559`  
		Last Modified: Tue, 26 May 2020 22:49:35 GMT  
		Size: 2.3 MB (2302081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7828b9f2b027f87ec1ac524c0a524c3376af9bc9d471ac9a00a5cab4281efb`  
		Last Modified: Tue, 26 May 2020 22:49:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22febb32fe4f36485028be48ce732295512c5149810cf2349b2de7d085e7a8a4`  
		Last Modified: Tue, 26 May 2020 23:34:20 GMT  
		Size: 800.1 KB (800061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d2fb5f67a5a20d1c98d85b204f33851f6fffffd8befbf7128e95984561a5c`  
		Last Modified: Tue, 26 May 2020 23:34:25 GMT  
		Size: 16.6 MB (16635028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e8766b8d75490a5b531617cc41b6ee20ae3fc3a43d9b9719c7cc4b47e882f8`  
		Last Modified: Tue, 26 May 2020 23:34:20 GMT  
		Size: 654.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66f4903743547fdc63285057966542fcfd6c4caf2dc657b26491ea87075535`  
		Last Modified: Tue, 26 May 2020 23:34:20 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:0.54.0`

```console
$ docker pull mongo-express@sha256:bef1da1e94ac497e2016429a4b9521e038fd0590f10c3853f4f6e69b8e1f8ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:0.54.0` - linux; amd64

```console
$ docker pull mongo-express@sha256:ee184818d2f005f223678830f0f8e1d09541fe33817c0580b6191135571477e7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47221155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae0a154c4d73f1e61a532148942c582fbfad22944638d4307a4710daa1398b6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2020 22:45:00 GMT
ENV NODE_VERSION=12.17.0
# Tue, 26 May 2020 22:45:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="fbd8916cc5a3c85dc503cc1fe9606cf8860152c4e8b2f2fcc729e48db3e3d654"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 26 May 2020 22:45:06 GMT
ENV YARN_VERSION=1.22.4
# Tue, 26 May 2020 22:45:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 26 May 2020 22:45:08 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 26 May 2020 22:45:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2020 22:45:09 GMT
CMD ["node"]
# Tue, 26 May 2020 23:04:16 GMT
RUN apk add --no-cache bash tini
# Tue, 26 May 2020 23:04:17 GMT
EXPOSE 8081
# Tue, 26 May 2020 23:04:17 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Tue, 26 May 2020 23:04:17 GMT
ENV MONGO_EXPRESS=0.54.0
# Tue, 26 May 2020 23:04:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Tue, 26 May 2020 23:04:50 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Tue, 26 May 2020 23:04:51 GMT
WORKDIR /node_modules/mongo-express
# Tue, 26 May 2020 23:04:52 GMT
RUN cp config.default.js config.js
# Tue, 26 May 2020 23:04:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2020 23:04:53 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2258f794beb1f503eb2951ce0825088dfaf1b1351cec61d423a9d36e6074ced`  
		Last Modified: Tue, 26 May 2020 22:48:30 GMT  
		Size: 24.7 MB (24740785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb2c1711f4234fb4ece973e4c6a76c536ea07629e4e1fe72d6e5f9def0100e`  
		Last Modified: Tue, 26 May 2020 22:48:23 GMT  
		Size: 2.2 MB (2239066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c89d818d1fec3df1d4a708492894de475c4daa5f8053a4d589d9b0484e2c099`  
		Last Modified: Tue, 26 May 2020 22:48:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98464beaa01d5bd3c3a3c5cc4bbed22fd85acf27795c921e4ac111bca94defbc`  
		Last Modified: Tue, 26 May 2020 23:05:08 GMT  
		Size: 789.2 KB (789191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46034b648892c97835f4629fee327f4d4080ac3632f797dbac7d2d6bda0064a`  
		Last Modified: Tue, 26 May 2020 23:05:12 GMT  
		Size: 16.6 MB (16634712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b1fb5cba44f347581ac773ce0354b354204635e5eee97d842e0e45525214fd`  
		Last Modified: Tue, 26 May 2020 23:05:06 GMT  
		Size: 655.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6590f2ff35b683538683ce843fe70b89d35fb04ee61aca34eb446213c0ca4eec`  
		Last Modified: Tue, 26 May 2020 23:05:06 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:0.54.0` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:d2c56758de742920482281e3a1949abcf2287e8f5226fb610d066e1a99c32036
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b30afdc3f8e4dfbda3f4a5f17dcfb432c21b8eb6741ff0dd235c5b11a5f9ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2020 22:31:07 GMT
ENV NODE_VERSION=12.17.0
# Tue, 26 May 2020 22:42:13 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="fbd8916cc5a3c85dc503cc1fe9606cf8860152c4e8b2f2fcc729e48db3e3d654"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 26 May 2020 22:42:16 GMT
ENV YARN_VERSION=1.22.4
# Tue, 26 May 2020 22:42:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 26 May 2020 22:42:28 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 26 May 2020 22:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2020 22:42:32 GMT
CMD ["node"]
# Tue, 26 May 2020 23:32:53 GMT
RUN apk add --no-cache bash tini
# Tue, 26 May 2020 23:32:56 GMT
EXPOSE 8081
# Tue, 26 May 2020 23:32:58 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Tue, 26 May 2020 23:33:00 GMT
ENV MONGO_EXPRESS=0.54.0
# Tue, 26 May 2020 23:33:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Tue, 26 May 2020 23:33:48 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Tue, 26 May 2020 23:33:50 GMT
WORKDIR /node_modules/mongo-express
# Tue, 26 May 2020 23:33:57 GMT
RUN cp config.default.js config.js
# Tue, 26 May 2020 23:33:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2020 23:33:59 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0645aba79184b4b2f8746b951cd4f319eaad9894739aa71726e80e7454bd7a`  
		Last Modified: Tue, 26 May 2020 22:49:44 GMT  
		Size: 24.9 MB (24864671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf79fc3473c4e5879fc6ec74fda103961b7e6a2c89dd7e21c06085e40ee2559`  
		Last Modified: Tue, 26 May 2020 22:49:35 GMT  
		Size: 2.3 MB (2302081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7828b9f2b027f87ec1ac524c0a524c3376af9bc9d471ac9a00a5cab4281efb`  
		Last Modified: Tue, 26 May 2020 22:49:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22febb32fe4f36485028be48ce732295512c5149810cf2349b2de7d085e7a8a4`  
		Last Modified: Tue, 26 May 2020 23:34:20 GMT  
		Size: 800.1 KB (800061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d2fb5f67a5a20d1c98d85b204f33851f6fffffd8befbf7128e95984561a5c`  
		Last Modified: Tue, 26 May 2020 23:34:25 GMT  
		Size: 16.6 MB (16635028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e8766b8d75490a5b531617cc41b6ee20ae3fc3a43d9b9719c7cc4b47e882f8`  
		Last Modified: Tue, 26 May 2020 23:34:20 GMT  
		Size: 654.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66f4903743547fdc63285057966542fcfd6c4caf2dc657b26491ea87075535`  
		Last Modified: Tue, 26 May 2020 23:34:20 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:latest`

```console
$ docker pull mongo-express@sha256:bef1da1e94ac497e2016429a4b9521e038fd0590f10c3853f4f6e69b8e1f8ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:latest` - linux; amd64

```console
$ docker pull mongo-express@sha256:ee184818d2f005f223678830f0f8e1d09541fe33817c0580b6191135571477e7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47221155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae0a154c4d73f1e61a532148942c582fbfad22944638d4307a4710daa1398b6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2020 22:45:00 GMT
ENV NODE_VERSION=12.17.0
# Tue, 26 May 2020 22:45:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="fbd8916cc5a3c85dc503cc1fe9606cf8860152c4e8b2f2fcc729e48db3e3d654"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 26 May 2020 22:45:06 GMT
ENV YARN_VERSION=1.22.4
# Tue, 26 May 2020 22:45:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 26 May 2020 22:45:08 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 26 May 2020 22:45:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2020 22:45:09 GMT
CMD ["node"]
# Tue, 26 May 2020 23:04:16 GMT
RUN apk add --no-cache bash tini
# Tue, 26 May 2020 23:04:17 GMT
EXPOSE 8081
# Tue, 26 May 2020 23:04:17 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Tue, 26 May 2020 23:04:17 GMT
ENV MONGO_EXPRESS=0.54.0
# Tue, 26 May 2020 23:04:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Tue, 26 May 2020 23:04:50 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Tue, 26 May 2020 23:04:51 GMT
WORKDIR /node_modules/mongo-express
# Tue, 26 May 2020 23:04:52 GMT
RUN cp config.default.js config.js
# Tue, 26 May 2020 23:04:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2020 23:04:53 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2258f794beb1f503eb2951ce0825088dfaf1b1351cec61d423a9d36e6074ced`  
		Last Modified: Tue, 26 May 2020 22:48:30 GMT  
		Size: 24.7 MB (24740785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb2c1711f4234fb4ece973e4c6a76c536ea07629e4e1fe72d6e5f9def0100e`  
		Last Modified: Tue, 26 May 2020 22:48:23 GMT  
		Size: 2.2 MB (2239066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c89d818d1fec3df1d4a708492894de475c4daa5f8053a4d589d9b0484e2c099`  
		Last Modified: Tue, 26 May 2020 22:48:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98464beaa01d5bd3c3a3c5cc4bbed22fd85acf27795c921e4ac111bca94defbc`  
		Last Modified: Tue, 26 May 2020 23:05:08 GMT  
		Size: 789.2 KB (789191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46034b648892c97835f4629fee327f4d4080ac3632f797dbac7d2d6bda0064a`  
		Last Modified: Tue, 26 May 2020 23:05:12 GMT  
		Size: 16.6 MB (16634712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b1fb5cba44f347581ac773ce0354b354204635e5eee97d842e0e45525214fd`  
		Last Modified: Tue, 26 May 2020 23:05:06 GMT  
		Size: 655.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6590f2ff35b683538683ce843fe70b89d35fb04ee61aca34eb446213c0ca4eec`  
		Last Modified: Tue, 26 May 2020 23:05:06 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:latest` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:d2c56758de742920482281e3a1949abcf2287e8f5226fb610d066e1a99c32036
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b30afdc3f8e4dfbda3f4a5f17dcfb432c21b8eb6741ff0dd235c5b11a5f9ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2020 22:31:07 GMT
ENV NODE_VERSION=12.17.0
# Tue, 26 May 2020 22:42:13 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="fbd8916cc5a3c85dc503cc1fe9606cf8860152c4e8b2f2fcc729e48db3e3d654"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Tue, 26 May 2020 22:42:16 GMT
ENV YARN_VERSION=1.22.4
# Tue, 26 May 2020 22:42:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Tue, 26 May 2020 22:42:28 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Tue, 26 May 2020 22:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2020 22:42:32 GMT
CMD ["node"]
# Tue, 26 May 2020 23:32:53 GMT
RUN apk add --no-cache bash tini
# Tue, 26 May 2020 23:32:56 GMT
EXPOSE 8081
# Tue, 26 May 2020 23:32:58 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Tue, 26 May 2020 23:33:00 GMT
ENV MONGO_EXPRESS=0.54.0
# Tue, 26 May 2020 23:33:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Tue, 26 May 2020 23:33:48 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Tue, 26 May 2020 23:33:50 GMT
WORKDIR /node_modules/mongo-express
# Tue, 26 May 2020 23:33:57 GMT
RUN cp config.default.js config.js
# Tue, 26 May 2020 23:33:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 26 May 2020 23:33:59 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0645aba79184b4b2f8746b951cd4f319eaad9894739aa71726e80e7454bd7a`  
		Last Modified: Tue, 26 May 2020 22:49:44 GMT  
		Size: 24.9 MB (24864671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf79fc3473c4e5879fc6ec74fda103961b7e6a2c89dd7e21c06085e40ee2559`  
		Last Modified: Tue, 26 May 2020 22:49:35 GMT  
		Size: 2.3 MB (2302081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7828b9f2b027f87ec1ac524c0a524c3376af9bc9d471ac9a00a5cab4281efb`  
		Last Modified: Tue, 26 May 2020 22:49:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22febb32fe4f36485028be48ce732295512c5149810cf2349b2de7d085e7a8a4`  
		Last Modified: Tue, 26 May 2020 23:34:20 GMT  
		Size: 800.1 KB (800061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d2fb5f67a5a20d1c98d85b204f33851f6fffffd8befbf7128e95984561a5c`  
		Last Modified: Tue, 26 May 2020 23:34:25 GMT  
		Size: 16.6 MB (16635028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e8766b8d75490a5b531617cc41b6ee20ae3fc3a43d9b9719c7cc4b47e882f8`  
		Last Modified: Tue, 26 May 2020 23:34:20 GMT  
		Size: 654.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66f4903743547fdc63285057966542fcfd6c4caf2dc657b26491ea87075535`  
		Last Modified: Tue, 26 May 2020 23:34:20 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
