<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo-express`

-	[`mongo-express:0.54`](#mongo-express054)
-	[`mongo-express:0.54.0`](#mongo-express0540)
-	[`mongo-express:latest`](#mongo-expresslatest)

## `mongo-express:0.54`

```console
$ docker pull mongo-express@sha256:c7de9be52e7f315cc230649cc2fa0c64cb9c3552d4db85a553e17de608804026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:0.54` - linux; amd64

```console
$ docker pull mongo-express@sha256:44caa8cb9c56ea0d6fc31a305bd1d564e1e287b10b1ce3535d31946058d996df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46568072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1c7f5f8b5449d5727dc62de58f88e36498a22223070464a8bcfa85e9ed0e76`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2020 19:46:49 GMT
ENV NODE_VERSION=12.16.2
# Thu, 09 Apr 2020 19:47:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="f6b8bb0ee376cd1e7096f15b68efc3bb6adbd2cb33a12002d5982384b733dcab"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 09 Apr 2020 19:47:00 GMT
ENV YARN_VERSION=1.22.4
# Thu, 09 Apr 2020 19:47:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 09 Apr 2020 19:47:05 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 09 Apr 2020 19:47:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2020 19:47:06 GMT
CMD ["node"]
# Thu, 09 Apr 2020 20:30:22 GMT
RUN apk add --no-cache bash tini
# Thu, 09 Apr 2020 20:30:23 GMT
EXPOSE 8081
# Thu, 09 Apr 2020 20:30:23 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 09 Apr 2020 20:30:23 GMT
ENV MONGO_EXPRESS=0.54.0
# Thu, 09 Apr 2020 20:30:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 09 Apr 2020 20:30:59 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Thu, 09 Apr 2020 20:30:59 GMT
WORKDIR /node_modules/mongo-express
# Thu, 09 Apr 2020 20:31:00 GMT
RUN cp config.default.js config.js
# Thu, 09 Apr 2020 20:31:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Apr 2020 20:31:01 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6875f31a79a89ba75198be98bcf8542ebf5bedc72e713643f8051c1de5f953`  
		Last Modified: Thu, 09 Apr 2020 19:52:56 GMT  
		Size: 24.6 MB (24575127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee60dddbbe0d354499cf6e1b0202cad13fc488549b4e4c7d8dcf6c2a1a03bbf`  
		Last Modified: Thu, 09 Apr 2020 19:52:49 GMT  
		Size: 2.2 MB (2239181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea56792bc485065256bba51dc1b589b188c453a852865d0b49d7736684ed33a6`  
		Last Modified: Thu, 09 Apr 2020 19:52:48 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417d4246e8d3538feb2e62119339edd11e595668a88e8bf28213bf5a4cab96bd`  
		Last Modified: Thu, 09 Apr 2020 20:31:12 GMT  
		Size: 789.2 KB (789200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02484ba5e0d0224b5288fdb2339bcfaf03ff2a4cedb439c654c3a809abc68eb8`  
		Last Modified: Thu, 09 Apr 2020 20:31:16 GMT  
		Size: 16.2 MB (16157223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c64e9ed4a113062c3d65adb6ce5a6d093137a44f52f8a8cf301db38ca3689`  
		Last Modified: Thu, 09 Apr 2020 20:31:12 GMT  
		Size: 655.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fce5780a016426bbc5775c513b02fcd555a976d45c615c03f852055f5ccdcab`  
		Last Modified: Thu, 09 Apr 2020 20:31:12 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:0.54` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a425fd4106363ead0b349e3bbf423019d6e18bbbabf8bbf8ae079e5202358319
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46721672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c31c7d188df0996e9896de6068cbecfbefca8af62583e97973bae14e3375b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2020 18:05:29 GMT
ENV NODE_VERSION=12.16.2
# Thu, 09 Apr 2020 18:17:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="f6b8bb0ee376cd1e7096f15b68efc3bb6adbd2cb33a12002d5982384b733dcab"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 09 Apr 2020 18:17:48 GMT
ENV YARN_VERSION=1.22.4
# Thu, 09 Apr 2020 18:17:53 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 09 Apr 2020 18:17:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 09 Apr 2020 18:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2020 18:17:55 GMT
CMD ["node"]
# Thu, 09 Apr 2020 18:39:50 GMT
RUN apk add --no-cache bash tini
# Thu, 09 Apr 2020 18:39:52 GMT
EXPOSE 8081
# Thu, 09 Apr 2020 18:39:53 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 09 Apr 2020 18:39:54 GMT
ENV MONGO_EXPRESS=0.54.0
# Thu, 09 Apr 2020 18:40:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 09 Apr 2020 18:40:38 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Thu, 09 Apr 2020 18:40:39 GMT
WORKDIR /node_modules/mongo-express
# Thu, 09 Apr 2020 18:40:44 GMT
RUN cp config.default.js config.js
# Thu, 09 Apr 2020 18:40:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Apr 2020 18:40:46 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695e551189cd0ee595a4bfa68fb097a011be1124a04463a9c25c3081bd1e92f8`  
		Last Modified: Thu, 09 Apr 2020 18:22:42 GMT  
		Size: 24.7 MB (24735479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9054bafad0b503cd31a36a93d80cdc6318e91b119295b36c0812aa3b266e9ff0`  
		Last Modified: Thu, 09 Apr 2020 18:22:33 GMT  
		Size: 2.3 MB (2302286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80ee948777ae708a28b028c090e78a3026ac1a5265708b0903b99aa4d209eea`  
		Last Modified: Thu, 09 Apr 2020 18:22:32 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6c2f818466da57190e4417e962d9b107153b3a8ee11028f41555dc40eee349`  
		Last Modified: Thu, 09 Apr 2020 18:41:04 GMT  
		Size: 800.1 KB (800058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9523fcd0fd7cb3a806844f5a7d6b35eba0ba37b515471f2209872374c3395104`  
		Last Modified: Thu, 09 Apr 2020 18:41:09 GMT  
		Size: 16.2 MB (16156627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260b411889d59dcf9a0370e8fc0a0ebbd7170ffacb3ca5dd1f54e352efd2881b`  
		Last Modified: Thu, 09 Apr 2020 18:41:04 GMT  
		Size: 656.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075f5c4084dbe3fe19d77e4812bb5b6bbf87821da4d1ab40da0ec2253669f05`  
		Last Modified: Thu, 09 Apr 2020 18:41:04 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:0.54.0`

```console
$ docker pull mongo-express@sha256:c7de9be52e7f315cc230649cc2fa0c64cb9c3552d4db85a553e17de608804026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:0.54.0` - linux; amd64

```console
$ docker pull mongo-express@sha256:44caa8cb9c56ea0d6fc31a305bd1d564e1e287b10b1ce3535d31946058d996df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46568072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1c7f5f8b5449d5727dc62de58f88e36498a22223070464a8bcfa85e9ed0e76`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2020 19:46:49 GMT
ENV NODE_VERSION=12.16.2
# Thu, 09 Apr 2020 19:47:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="f6b8bb0ee376cd1e7096f15b68efc3bb6adbd2cb33a12002d5982384b733dcab"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 09 Apr 2020 19:47:00 GMT
ENV YARN_VERSION=1.22.4
# Thu, 09 Apr 2020 19:47:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 09 Apr 2020 19:47:05 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 09 Apr 2020 19:47:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2020 19:47:06 GMT
CMD ["node"]
# Thu, 09 Apr 2020 20:30:22 GMT
RUN apk add --no-cache bash tini
# Thu, 09 Apr 2020 20:30:23 GMT
EXPOSE 8081
# Thu, 09 Apr 2020 20:30:23 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 09 Apr 2020 20:30:23 GMT
ENV MONGO_EXPRESS=0.54.0
# Thu, 09 Apr 2020 20:30:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 09 Apr 2020 20:30:59 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Thu, 09 Apr 2020 20:30:59 GMT
WORKDIR /node_modules/mongo-express
# Thu, 09 Apr 2020 20:31:00 GMT
RUN cp config.default.js config.js
# Thu, 09 Apr 2020 20:31:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Apr 2020 20:31:01 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6875f31a79a89ba75198be98bcf8542ebf5bedc72e713643f8051c1de5f953`  
		Last Modified: Thu, 09 Apr 2020 19:52:56 GMT  
		Size: 24.6 MB (24575127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee60dddbbe0d354499cf6e1b0202cad13fc488549b4e4c7d8dcf6c2a1a03bbf`  
		Last Modified: Thu, 09 Apr 2020 19:52:49 GMT  
		Size: 2.2 MB (2239181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea56792bc485065256bba51dc1b589b188c453a852865d0b49d7736684ed33a6`  
		Last Modified: Thu, 09 Apr 2020 19:52:48 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417d4246e8d3538feb2e62119339edd11e595668a88e8bf28213bf5a4cab96bd`  
		Last Modified: Thu, 09 Apr 2020 20:31:12 GMT  
		Size: 789.2 KB (789200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02484ba5e0d0224b5288fdb2339bcfaf03ff2a4cedb439c654c3a809abc68eb8`  
		Last Modified: Thu, 09 Apr 2020 20:31:16 GMT  
		Size: 16.2 MB (16157223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c64e9ed4a113062c3d65adb6ce5a6d093137a44f52f8a8cf301db38ca3689`  
		Last Modified: Thu, 09 Apr 2020 20:31:12 GMT  
		Size: 655.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fce5780a016426bbc5775c513b02fcd555a976d45c615c03f852055f5ccdcab`  
		Last Modified: Thu, 09 Apr 2020 20:31:12 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:0.54.0` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a425fd4106363ead0b349e3bbf423019d6e18bbbabf8bbf8ae079e5202358319
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46721672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c31c7d188df0996e9896de6068cbecfbefca8af62583e97973bae14e3375b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2020 18:05:29 GMT
ENV NODE_VERSION=12.16.2
# Thu, 09 Apr 2020 18:17:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="f6b8bb0ee376cd1e7096f15b68efc3bb6adbd2cb33a12002d5982384b733dcab"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 09 Apr 2020 18:17:48 GMT
ENV YARN_VERSION=1.22.4
# Thu, 09 Apr 2020 18:17:53 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 09 Apr 2020 18:17:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 09 Apr 2020 18:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2020 18:17:55 GMT
CMD ["node"]
# Thu, 09 Apr 2020 18:39:50 GMT
RUN apk add --no-cache bash tini
# Thu, 09 Apr 2020 18:39:52 GMT
EXPOSE 8081
# Thu, 09 Apr 2020 18:39:53 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 09 Apr 2020 18:39:54 GMT
ENV MONGO_EXPRESS=0.54.0
# Thu, 09 Apr 2020 18:40:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 09 Apr 2020 18:40:38 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Thu, 09 Apr 2020 18:40:39 GMT
WORKDIR /node_modules/mongo-express
# Thu, 09 Apr 2020 18:40:44 GMT
RUN cp config.default.js config.js
# Thu, 09 Apr 2020 18:40:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Apr 2020 18:40:46 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695e551189cd0ee595a4bfa68fb097a011be1124a04463a9c25c3081bd1e92f8`  
		Last Modified: Thu, 09 Apr 2020 18:22:42 GMT  
		Size: 24.7 MB (24735479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9054bafad0b503cd31a36a93d80cdc6318e91b119295b36c0812aa3b266e9ff0`  
		Last Modified: Thu, 09 Apr 2020 18:22:33 GMT  
		Size: 2.3 MB (2302286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80ee948777ae708a28b028c090e78a3026ac1a5265708b0903b99aa4d209eea`  
		Last Modified: Thu, 09 Apr 2020 18:22:32 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6c2f818466da57190e4417e962d9b107153b3a8ee11028f41555dc40eee349`  
		Last Modified: Thu, 09 Apr 2020 18:41:04 GMT  
		Size: 800.1 KB (800058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9523fcd0fd7cb3a806844f5a7d6b35eba0ba37b515471f2209872374c3395104`  
		Last Modified: Thu, 09 Apr 2020 18:41:09 GMT  
		Size: 16.2 MB (16156627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260b411889d59dcf9a0370e8fc0a0ebbd7170ffacb3ca5dd1f54e352efd2881b`  
		Last Modified: Thu, 09 Apr 2020 18:41:04 GMT  
		Size: 656.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075f5c4084dbe3fe19d77e4812bb5b6bbf87821da4d1ab40da0ec2253669f05`  
		Last Modified: Thu, 09 Apr 2020 18:41:04 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:latest`

```console
$ docker pull mongo-express@sha256:c7de9be52e7f315cc230649cc2fa0c64cb9c3552d4db85a553e17de608804026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:latest` - linux; amd64

```console
$ docker pull mongo-express@sha256:44caa8cb9c56ea0d6fc31a305bd1d564e1e287b10b1ce3535d31946058d996df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46568072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1c7f5f8b5449d5727dc62de58f88e36498a22223070464a8bcfa85e9ed0e76`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2020 19:46:49 GMT
ENV NODE_VERSION=12.16.2
# Thu, 09 Apr 2020 19:47:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="f6b8bb0ee376cd1e7096f15b68efc3bb6adbd2cb33a12002d5982384b733dcab"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 09 Apr 2020 19:47:00 GMT
ENV YARN_VERSION=1.22.4
# Thu, 09 Apr 2020 19:47:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 09 Apr 2020 19:47:05 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 09 Apr 2020 19:47:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2020 19:47:06 GMT
CMD ["node"]
# Thu, 09 Apr 2020 20:30:22 GMT
RUN apk add --no-cache bash tini
# Thu, 09 Apr 2020 20:30:23 GMT
EXPOSE 8081
# Thu, 09 Apr 2020 20:30:23 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 09 Apr 2020 20:30:23 GMT
ENV MONGO_EXPRESS=0.54.0
# Thu, 09 Apr 2020 20:30:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 09 Apr 2020 20:30:59 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Thu, 09 Apr 2020 20:30:59 GMT
WORKDIR /node_modules/mongo-express
# Thu, 09 Apr 2020 20:31:00 GMT
RUN cp config.default.js config.js
# Thu, 09 Apr 2020 20:31:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Apr 2020 20:31:01 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6875f31a79a89ba75198be98bcf8542ebf5bedc72e713643f8051c1de5f953`  
		Last Modified: Thu, 09 Apr 2020 19:52:56 GMT  
		Size: 24.6 MB (24575127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee60dddbbe0d354499cf6e1b0202cad13fc488549b4e4c7d8dcf6c2a1a03bbf`  
		Last Modified: Thu, 09 Apr 2020 19:52:49 GMT  
		Size: 2.2 MB (2239181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea56792bc485065256bba51dc1b589b188c453a852865d0b49d7736684ed33a6`  
		Last Modified: Thu, 09 Apr 2020 19:52:48 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417d4246e8d3538feb2e62119339edd11e595668a88e8bf28213bf5a4cab96bd`  
		Last Modified: Thu, 09 Apr 2020 20:31:12 GMT  
		Size: 789.2 KB (789200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02484ba5e0d0224b5288fdb2339bcfaf03ff2a4cedb439c654c3a809abc68eb8`  
		Last Modified: Thu, 09 Apr 2020 20:31:16 GMT  
		Size: 16.2 MB (16157223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c64e9ed4a113062c3d65adb6ce5a6d093137a44f52f8a8cf301db38ca3689`  
		Last Modified: Thu, 09 Apr 2020 20:31:12 GMT  
		Size: 655.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fce5780a016426bbc5775c513b02fcd555a976d45c615c03f852055f5ccdcab`  
		Last Modified: Thu, 09 Apr 2020 20:31:12 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:latest` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a425fd4106363ead0b349e3bbf423019d6e18bbbabf8bbf8ae079e5202358319
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46721672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c31c7d188df0996e9896de6068cbecfbefca8af62583e97973bae14e3375b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2020 18:05:29 GMT
ENV NODE_VERSION=12.16.2
# Thu, 09 Apr 2020 18:17:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="f6b8bb0ee376cd1e7096f15b68efc3bb6adbd2cb33a12002d5982384b733dcab"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Thu, 09 Apr 2020 18:17:48 GMT
ENV YARN_VERSION=1.22.4
# Thu, 09 Apr 2020 18:17:53 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Thu, 09 Apr 2020 18:17:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Thu, 09 Apr 2020 18:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2020 18:17:55 GMT
CMD ["node"]
# Thu, 09 Apr 2020 18:39:50 GMT
RUN apk add --no-cache bash tini
# Thu, 09 Apr 2020 18:39:52 GMT
EXPOSE 8081
# Thu, 09 Apr 2020 18:39:53 GMT
ENV ME_CONFIG_EDITORTHEME=default ME_CONFIG_MONGODB_SERVER=mongo ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_BASICAUTH_USERNAME= ME_CONFIG_BASICAUTH_PASSWORD= VCAP_APP_HOST=0.0.0.0
# Thu, 09 Apr 2020 18:39:54 GMT
ENV MONGO_EXPRESS=0.54.0
# Thu, 09 Apr 2020 18:40:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .me-install-deps git; 	npm install mongo-express@$MONGO_EXPRESS; 	apk del --no-network .me-install-deps
# Thu, 09 Apr 2020 18:40:38 GMT
COPY file:ad71ad0a2a1967b86be9140686f9a9aa6f78dc470d2ec9de89cbf1a25e85b550 in / 
# Thu, 09 Apr 2020 18:40:39 GMT
WORKDIR /node_modules/mongo-express
# Thu, 09 Apr 2020 18:40:44 GMT
RUN cp config.default.js config.js
# Thu, 09 Apr 2020 18:40:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Apr 2020 18:40:46 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695e551189cd0ee595a4bfa68fb097a011be1124a04463a9c25c3081bd1e92f8`  
		Last Modified: Thu, 09 Apr 2020 18:22:42 GMT  
		Size: 24.7 MB (24735479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9054bafad0b503cd31a36a93d80cdc6318e91b119295b36c0812aa3b266e9ff0`  
		Last Modified: Thu, 09 Apr 2020 18:22:33 GMT  
		Size: 2.3 MB (2302286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80ee948777ae708a28b028c090e78a3026ac1a5265708b0903b99aa4d209eea`  
		Last Modified: Thu, 09 Apr 2020 18:22:32 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6c2f818466da57190e4417e962d9b107153b3a8ee11028f41555dc40eee349`  
		Last Modified: Thu, 09 Apr 2020 18:41:04 GMT  
		Size: 800.1 KB (800058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9523fcd0fd7cb3a806844f5a7d6b35eba0ba37b515471f2209872374c3395104`  
		Last Modified: Thu, 09 Apr 2020 18:41:09 GMT  
		Size: 16.2 MB (16156627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260b411889d59dcf9a0370e8fc0a0ebbd7170ffacb3ca5dd1f54e352efd2881b`  
		Last Modified: Thu, 09 Apr 2020 18:41:04 GMT  
		Size: 656.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d075f5c4084dbe3fe19d77e4812bb5b6bbf87821da4d1ab40da0ec2253669f05`  
		Last Modified: Thu, 09 Apr 2020 18:41:04 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
