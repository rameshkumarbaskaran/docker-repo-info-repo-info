<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:2`](#rocketchat2)
-	[`rocket.chat:2.4`](#rocketchat24)
-	[`rocket.chat:2.4.12`](#rocketchat2412)
-	[`rocket.chat:3`](#rocketchat3)
-	[`rocket.chat:3.7`](#rocketchat37)
-	[`rocket.chat:3.7.1`](#rocketchat371)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:2`

```console
$ docker pull rocket.chat@sha256:72be4658e3be8510fa24d1f425747ca0ec8ea6e8ac8d743326fd260fa975aa11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:99e0947c9b462cd11bbf1ce424ac0486c1aad739dfd234a32ec1dcfa6ce37529
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230183904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3914124a46d03bf0c2b8c908d00b7096be2c1dc175ca579001653279ef9c4f`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:05:58 GMT
ENV NODE_ENV=production
# Thu, 10 Sep 2020 19:07:44 GMT
ENV NODE_VERSION=8.17.0
# Thu, 10 Sep 2020 19:08:01 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 10 Sep 2020 19:08:02 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Thu, 10 Sep 2020 19:08:03 GMT
VOLUME [/app/uploads]
# Thu, 10 Sep 2020 19:08:03 GMT
ENV RC_VERSION=2.4.12
# Thu, 10 Sep 2020 19:08:03 GMT
WORKDIR /app
# Thu, 10 Sep 2020 19:09:04 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends ca-certificates curl gnupg &&  gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Thu, 10 Sep 2020 19:09:06 GMT
USER rocketchat
# Thu, 10 Sep 2020 19:09:06 GMT
WORKDIR /app/bundle
# Thu, 10 Sep 2020 19:09:06 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 10 Sep 2020 19:09:07 GMT
EXPOSE 3000
# Thu, 10 Sep 2020 19:09:07 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee7f2e5cc2e20e60aa0567adefd137ac47b40d2833151fa54dc9141c403cf41`  
		Last Modified: Thu, 10 Sep 2020 19:10:18 GMT  
		Size: 19.8 MB (19785458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976aedfdc990611e6e63cedba3a6eb5d2dcae9abfa6a2ce22e0ed366a87a9c70`  
		Last Modified: Thu, 10 Sep 2020 19:10:13 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a6f44527cbfd5be6900bcd02fd03ec689230f07a92104f3d2fcff884d54a0`  
		Last Modified: Thu, 10 Sep 2020 19:10:59 GMT  
		Size: 183.3 MB (183304501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:2.4`

```console
$ docker pull rocket.chat@sha256:72be4658e3be8510fa24d1f425747ca0ec8ea6e8ac8d743326fd260fa975aa11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:2.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:99e0947c9b462cd11bbf1ce424ac0486c1aad739dfd234a32ec1dcfa6ce37529
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230183904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3914124a46d03bf0c2b8c908d00b7096be2c1dc175ca579001653279ef9c4f`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:05:58 GMT
ENV NODE_ENV=production
# Thu, 10 Sep 2020 19:07:44 GMT
ENV NODE_VERSION=8.17.0
# Thu, 10 Sep 2020 19:08:01 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 10 Sep 2020 19:08:02 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Thu, 10 Sep 2020 19:08:03 GMT
VOLUME [/app/uploads]
# Thu, 10 Sep 2020 19:08:03 GMT
ENV RC_VERSION=2.4.12
# Thu, 10 Sep 2020 19:08:03 GMT
WORKDIR /app
# Thu, 10 Sep 2020 19:09:04 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends ca-certificates curl gnupg &&  gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Thu, 10 Sep 2020 19:09:06 GMT
USER rocketchat
# Thu, 10 Sep 2020 19:09:06 GMT
WORKDIR /app/bundle
# Thu, 10 Sep 2020 19:09:06 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 10 Sep 2020 19:09:07 GMT
EXPOSE 3000
# Thu, 10 Sep 2020 19:09:07 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee7f2e5cc2e20e60aa0567adefd137ac47b40d2833151fa54dc9141c403cf41`  
		Last Modified: Thu, 10 Sep 2020 19:10:18 GMT  
		Size: 19.8 MB (19785458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976aedfdc990611e6e63cedba3a6eb5d2dcae9abfa6a2ce22e0ed366a87a9c70`  
		Last Modified: Thu, 10 Sep 2020 19:10:13 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a6f44527cbfd5be6900bcd02fd03ec689230f07a92104f3d2fcff884d54a0`  
		Last Modified: Thu, 10 Sep 2020 19:10:59 GMT  
		Size: 183.3 MB (183304501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:2.4.12`

```console
$ docker pull rocket.chat@sha256:72be4658e3be8510fa24d1f425747ca0ec8ea6e8ac8d743326fd260fa975aa11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:2.4.12` - linux; amd64

```console
$ docker pull rocket.chat@sha256:99e0947c9b462cd11bbf1ce424ac0486c1aad739dfd234a32ec1dcfa6ce37529
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230183904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3914124a46d03bf0c2b8c908d00b7096be2c1dc175ca579001653279ef9c4f`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:05:58 GMT
ENV NODE_ENV=production
# Thu, 10 Sep 2020 19:07:44 GMT
ENV NODE_VERSION=8.17.0
# Thu, 10 Sep 2020 19:08:01 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 10 Sep 2020 19:08:02 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Thu, 10 Sep 2020 19:08:03 GMT
VOLUME [/app/uploads]
# Thu, 10 Sep 2020 19:08:03 GMT
ENV RC_VERSION=2.4.12
# Thu, 10 Sep 2020 19:08:03 GMT
WORKDIR /app
# Thu, 10 Sep 2020 19:09:04 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends ca-certificates curl gnupg &&  gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Thu, 10 Sep 2020 19:09:06 GMT
USER rocketchat
# Thu, 10 Sep 2020 19:09:06 GMT
WORKDIR /app/bundle
# Thu, 10 Sep 2020 19:09:06 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 10 Sep 2020 19:09:07 GMT
EXPOSE 3000
# Thu, 10 Sep 2020 19:09:07 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee7f2e5cc2e20e60aa0567adefd137ac47b40d2833151fa54dc9141c403cf41`  
		Last Modified: Thu, 10 Sep 2020 19:10:18 GMT  
		Size: 19.8 MB (19785458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976aedfdc990611e6e63cedba3a6eb5d2dcae9abfa6a2ce22e0ed366a87a9c70`  
		Last Modified: Thu, 10 Sep 2020 19:10:13 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a6f44527cbfd5be6900bcd02fd03ec689230f07a92104f3d2fcff884d54a0`  
		Last Modified: Thu, 10 Sep 2020 19:10:59 GMT  
		Size: 183.3 MB (183304501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:3`

```console
$ docker pull rocket.chat@sha256:8c16735e7c79a567c79c48c210d1485e6ce63b6133272c751150f93cdf18c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2db0514069959b6d071a8e0b4ed78d8f76b2bb3ed6fbb050b8a77af2c5890ad0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240253452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ceb3a1986d8d3b886946e7356f1b54a168e5fb80ed812e54bde0bf1f2f9c24e`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:05:58 GMT
ENV NODE_ENV=production
# Wed, 30 Sep 2020 00:31:01 GMT
ENV NODE_VERSION=12.18.4
# Wed, 30 Sep 2020 00:31:16 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 30 Sep 2020 00:31:17 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Wed, 30 Sep 2020 00:31:17 GMT
VOLUME [/app/uploads]
# Mon, 12 Oct 2020 17:42:24 GMT
ENV RC_VERSION=3.7.1
# Mon, 12 Oct 2020 17:42:25 GMT
WORKDIR /app
# Mon, 12 Oct 2020 17:43:43 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg &&  gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Mon, 12 Oct 2020 17:43:45 GMT
USER rocketchat
# Mon, 12 Oct 2020 17:43:45 GMT
WORKDIR /app/bundle
# Mon, 12 Oct 2020 17:43:45 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 12 Oct 2020 17:43:46 GMT
EXPOSE 3000
# Mon, 12 Oct 2020 17:43:46 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addff3b2b7eba6d4f77db7d31d76a3ec0333f8487d98db8b6f898ecdfd9f755a`  
		Last Modified: Wed, 30 Sep 2020 00:32:46 GMT  
		Size: 24.2 MB (24207873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ff7511ff2b82c81009cd1699ca70ffc14bfd7e76f8fd736a0c564a4d532b67`  
		Last Modified: Wed, 30 Sep 2020 00:32:41 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5e40b3f100ea7e211854dcaf9c90bb7ad18144ef9cb85282f7c005f9ced0e2`  
		Last Modified: Mon, 12 Oct 2020 17:44:54 GMT  
		Size: 189.0 MB (188951637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:3.7`

```console
$ docker pull rocket.chat@sha256:8c16735e7c79a567c79c48c210d1485e6ce63b6133272c751150f93cdf18c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:3.7` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2db0514069959b6d071a8e0b4ed78d8f76b2bb3ed6fbb050b8a77af2c5890ad0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240253452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ceb3a1986d8d3b886946e7356f1b54a168e5fb80ed812e54bde0bf1f2f9c24e`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:05:58 GMT
ENV NODE_ENV=production
# Wed, 30 Sep 2020 00:31:01 GMT
ENV NODE_VERSION=12.18.4
# Wed, 30 Sep 2020 00:31:16 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 30 Sep 2020 00:31:17 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Wed, 30 Sep 2020 00:31:17 GMT
VOLUME [/app/uploads]
# Mon, 12 Oct 2020 17:42:24 GMT
ENV RC_VERSION=3.7.1
# Mon, 12 Oct 2020 17:42:25 GMT
WORKDIR /app
# Mon, 12 Oct 2020 17:43:43 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg &&  gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Mon, 12 Oct 2020 17:43:45 GMT
USER rocketchat
# Mon, 12 Oct 2020 17:43:45 GMT
WORKDIR /app/bundle
# Mon, 12 Oct 2020 17:43:45 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 12 Oct 2020 17:43:46 GMT
EXPOSE 3000
# Mon, 12 Oct 2020 17:43:46 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addff3b2b7eba6d4f77db7d31d76a3ec0333f8487d98db8b6f898ecdfd9f755a`  
		Last Modified: Wed, 30 Sep 2020 00:32:46 GMT  
		Size: 24.2 MB (24207873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ff7511ff2b82c81009cd1699ca70ffc14bfd7e76f8fd736a0c564a4d532b67`  
		Last Modified: Wed, 30 Sep 2020 00:32:41 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5e40b3f100ea7e211854dcaf9c90bb7ad18144ef9cb85282f7c005f9ced0e2`  
		Last Modified: Mon, 12 Oct 2020 17:44:54 GMT  
		Size: 189.0 MB (188951637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:3.7.1`

```console
$ docker pull rocket.chat@sha256:8c16735e7c79a567c79c48c210d1485e6ce63b6133272c751150f93cdf18c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:3.7.1` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2db0514069959b6d071a8e0b4ed78d8f76b2bb3ed6fbb050b8a77af2c5890ad0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240253452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ceb3a1986d8d3b886946e7356f1b54a168e5fb80ed812e54bde0bf1f2f9c24e`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:05:58 GMT
ENV NODE_ENV=production
# Wed, 30 Sep 2020 00:31:01 GMT
ENV NODE_VERSION=12.18.4
# Wed, 30 Sep 2020 00:31:16 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 30 Sep 2020 00:31:17 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Wed, 30 Sep 2020 00:31:17 GMT
VOLUME [/app/uploads]
# Mon, 12 Oct 2020 17:42:24 GMT
ENV RC_VERSION=3.7.1
# Mon, 12 Oct 2020 17:42:25 GMT
WORKDIR /app
# Mon, 12 Oct 2020 17:43:43 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg &&  gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Mon, 12 Oct 2020 17:43:45 GMT
USER rocketchat
# Mon, 12 Oct 2020 17:43:45 GMT
WORKDIR /app/bundle
# Mon, 12 Oct 2020 17:43:45 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 12 Oct 2020 17:43:46 GMT
EXPOSE 3000
# Mon, 12 Oct 2020 17:43:46 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addff3b2b7eba6d4f77db7d31d76a3ec0333f8487d98db8b6f898ecdfd9f755a`  
		Last Modified: Wed, 30 Sep 2020 00:32:46 GMT  
		Size: 24.2 MB (24207873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ff7511ff2b82c81009cd1699ca70ffc14bfd7e76f8fd736a0c564a4d532b67`  
		Last Modified: Wed, 30 Sep 2020 00:32:41 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5e40b3f100ea7e211854dcaf9c90bb7ad18144ef9cb85282f7c005f9ced0e2`  
		Last Modified: Mon, 12 Oct 2020 17:44:54 GMT  
		Size: 189.0 MB (188951637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:8c16735e7c79a567c79c48c210d1485e6ce63b6133272c751150f93cdf18c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:2db0514069959b6d071a8e0b4ed78d8f76b2bb3ed6fbb050b8a77af2c5890ad0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240253452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ceb3a1986d8d3b886946e7356f1b54a168e5fb80ed812e54bde0bf1f2f9c24e`
-	Default Command: `["node","main.js"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 19:05:58 GMT
ENV NODE_ENV=production
# Wed, 30 Sep 2020 00:31:01 GMT
ENV NODE_VERSION=12.18.4
# Wed, 30 Sep 2020 00:31:16 GMT
RUN ARCH="x64"     && set -eux     && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils     && rm -rf /var/lib/apt/lists/*     && for key in       94AE36675C464D64BAFA68DD7434390BDBE9B9C5       FD3A5288F042B6850C66B31F09FE44734EB7990E       71DCFD284A79C3B38668286BC97EC7A07EDE3FC1       DD8F2338BAE7501E3DD5AC78C273792F7D83545D       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       B9AE9905FFD7803F25714661B63B535A4C206CA9       77984A986EBC2AA786BC0F66B01FBB92821C587A       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       4ED778F539E3634C779C87C6D7062848A1AB005C       A48C2BEE680E841632CD4E44F07496B3EB3C1762       B9E2F5981AA6E0CD28160D9FF13993A75599653C     ; do       gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||       gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||       gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { print $(NF-1) }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 30 Sep 2020 00:31:17 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat:rocketchat /app/uploads
# Wed, 30 Sep 2020 00:31:17 GMT
VOLUME [/app/uploads]
# Mon, 12 Oct 2020 17:42:24 GMT
ENV RC_VERSION=3.7.1
# Mon, 12 Oct 2020 17:42:25 GMT
WORKDIR /app
# Mon, 12 Oct 2020 17:43:43 GMT
RUN set -eux &&  apt-get update &&  apt-get install -y --no-install-recommends fontconfig &&  aptMark="$(apt-mark showmanual)" &&  apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg &&  gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104 &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install &&  apt-mark auto '.*' > /dev/null &&  apt-mark manual $aptMark > /dev/null &&  find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { print $(NF-1) }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual &&  apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false &&  npm cache clear --force &&  chown -R rocketchat:rocketchat /app
# Mon, 12 Oct 2020 17:43:45 GMT
USER rocketchat
# Mon, 12 Oct 2020 17:43:45 GMT
WORKDIR /app/bundle
# Mon, 12 Oct 2020 17:43:45 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Mon, 12 Oct 2020 17:43:46 GMT
EXPOSE 3000
# Mon, 12 Oct 2020 17:43:46 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addff3b2b7eba6d4f77db7d31d76a3ec0333f8487d98db8b6f898ecdfd9f755a`  
		Last Modified: Wed, 30 Sep 2020 00:32:46 GMT  
		Size: 24.2 MB (24207873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ff7511ff2b82c81009cd1699ca70ffc14bfd7e76f8fd736a0c564a4d532b67`  
		Last Modified: Wed, 30 Sep 2020 00:32:41 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5e40b3f100ea7e211854dcaf9c90bb7ad18144ef9cb85282f7c005f9ced0e2`  
		Last Modified: Mon, 12 Oct 2020 17:44:54 GMT  
		Size: 189.0 MB (188951637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
