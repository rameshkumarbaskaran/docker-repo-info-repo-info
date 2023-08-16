<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:5`](#rocketchat5)
-	[`rocket.chat:5.4`](#rocketchat54)
-	[`rocket.chat:5.4.10`](#rocketchat5410)
-	[`rocket.chat:6`](#rocketchat6)
-	[`rocket.chat:6.2`](#rocketchat62)
-	[`rocket.chat:6.2.12`](#rocketchat6212)
-	[`rocket.chat:6.3`](#rocketchat63)
-	[`rocket.chat:6.3.1`](#rocketchat631)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:5`

```console
$ docker pull rocket.chat@sha256:eb01fdac977cfb1dae8bcd051c3e96188560e1813a276f409f45063d8cb199a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5` - linux; amd64

```console
$ docker pull rocket.chat@sha256:d548b621200a8132f28d6c95ce8915299b0ac1a022da1d357db70caebe53a55c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301507167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3838ead6d167b45fbbe4fe60f7bff4bd610de392dbba7d97619712a097c4f09`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_ENV=production
# Wed, 16 Aug 2023 06:18:04 GMT
ENV NODE_VERSION=14.19.3
# Wed, 16 Aug 2023 06:18:27 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 06:18:28 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 16 Aug 2023 06:18:28 GMT
VOLUME [/app/uploads]
# Wed, 16 Aug 2023 06:18:28 GMT
ENV RC_VERSION=5.4.10
# Wed, 16 Aug 2023 06:18:28 GMT
WORKDIR /app
# Wed, 16 Aug 2023 06:19:32 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 16 Aug 2023 06:19:36 GMT
USER rocketchat
# Wed, 16 Aug 2023 06:19:36 GMT
WORKDIR /app/bundle
# Wed, 16 Aug 2023 06:19:36 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 16 Aug 2023 06:19:36 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 06:19:36 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e749ab26499ebd6fef67e55370c9bc6dd7dfc3ebba15254fb35f66fe765d47d6`  
		Last Modified: Wed, 16 Aug 2023 06:21:48 GMT  
		Size: 36.0 MB (36025236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7c26aca8418c145724e8bde1029eb25ae9d4f20fd6bc28a70982d0397af682`  
		Last Modified: Wed, 16 Aug 2023 06:21:42 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4718b5f57990aef406c5054f5064a0ca22b13506b06b4eb2c974b724127a3ecc`  
		Last Modified: Wed, 16 Aug 2023 06:22:23 GMT  
		Size: 238.3 MB (238292696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:5.4`

```console
$ docker pull rocket.chat@sha256:eb01fdac977cfb1dae8bcd051c3e96188560e1813a276f409f45063d8cb199a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5.4` - linux; amd64

```console
$ docker pull rocket.chat@sha256:d548b621200a8132f28d6c95ce8915299b0ac1a022da1d357db70caebe53a55c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301507167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3838ead6d167b45fbbe4fe60f7bff4bd610de392dbba7d97619712a097c4f09`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_ENV=production
# Wed, 16 Aug 2023 06:18:04 GMT
ENV NODE_VERSION=14.19.3
# Wed, 16 Aug 2023 06:18:27 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 06:18:28 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 16 Aug 2023 06:18:28 GMT
VOLUME [/app/uploads]
# Wed, 16 Aug 2023 06:18:28 GMT
ENV RC_VERSION=5.4.10
# Wed, 16 Aug 2023 06:18:28 GMT
WORKDIR /app
# Wed, 16 Aug 2023 06:19:32 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 16 Aug 2023 06:19:36 GMT
USER rocketchat
# Wed, 16 Aug 2023 06:19:36 GMT
WORKDIR /app/bundle
# Wed, 16 Aug 2023 06:19:36 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 16 Aug 2023 06:19:36 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 06:19:36 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e749ab26499ebd6fef67e55370c9bc6dd7dfc3ebba15254fb35f66fe765d47d6`  
		Last Modified: Wed, 16 Aug 2023 06:21:48 GMT  
		Size: 36.0 MB (36025236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7c26aca8418c145724e8bde1029eb25ae9d4f20fd6bc28a70982d0397af682`  
		Last Modified: Wed, 16 Aug 2023 06:21:42 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4718b5f57990aef406c5054f5064a0ca22b13506b06b4eb2c974b724127a3ecc`  
		Last Modified: Wed, 16 Aug 2023 06:22:23 GMT  
		Size: 238.3 MB (238292696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:5.4.10`

```console
$ docker pull rocket.chat@sha256:eb01fdac977cfb1dae8bcd051c3e96188560e1813a276f409f45063d8cb199a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:5.4.10` - linux; amd64

```console
$ docker pull rocket.chat@sha256:d548b621200a8132f28d6c95ce8915299b0ac1a022da1d357db70caebe53a55c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301507167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3838ead6d167b45fbbe4fe60f7bff4bd610de392dbba7d97619712a097c4f09`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_ENV=production
# Wed, 16 Aug 2023 06:18:04 GMT
ENV NODE_VERSION=14.19.3
# Wed, 16 Aug 2023 06:18:27 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 06:18:28 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 16 Aug 2023 06:18:28 GMT
VOLUME [/app/uploads]
# Wed, 16 Aug 2023 06:18:28 GMT
ENV RC_VERSION=5.4.10
# Wed, 16 Aug 2023 06:18:28 GMT
WORKDIR /app
# Wed, 16 Aug 2023 06:19:32 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 16 Aug 2023 06:19:36 GMT
USER rocketchat
# Wed, 16 Aug 2023 06:19:36 GMT
WORKDIR /app/bundle
# Wed, 16 Aug 2023 06:19:36 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 16 Aug 2023 06:19:36 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 06:19:36 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e749ab26499ebd6fef67e55370c9bc6dd7dfc3ebba15254fb35f66fe765d47d6`  
		Last Modified: Wed, 16 Aug 2023 06:21:48 GMT  
		Size: 36.0 MB (36025236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7c26aca8418c145724e8bde1029eb25ae9d4f20fd6bc28a70982d0397af682`  
		Last Modified: Wed, 16 Aug 2023 06:21:42 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4718b5f57990aef406c5054f5064a0ca22b13506b06b4eb2c974b724127a3ecc`  
		Last Modified: Wed, 16 Aug 2023 06:22:23 GMT  
		Size: 238.3 MB (238292696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6`

```console
$ docker pull rocket.chat@sha256:5f440075fa770ece6fa4edddb6195c68c0a5db231f7cada19578d540af82cc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3ece8402f9d5bf2df2ed0d2aa55eba7650bf56b9daed09f6ccc0f98118905f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320197166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7787de131f1ec7cd252a34296f5c9a2f74bf6a1835fe3f35c79975b326907fa1`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_ENV=production
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_VERSION=14.21.3
# Wed, 16 Aug 2023 06:15:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 06:15:13 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 16 Aug 2023 06:15:13 GMT
VOLUME [/app/uploads]
# Wed, 16 Aug 2023 06:15:13 GMT
ENV RC_VERSION=6.3.1
# Wed, 16 Aug 2023 06:15:13 GMT
WORKDIR /app
# Wed, 16 Aug 2023 06:16:15 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 16 Aug 2023 06:16:20 GMT
USER rocketchat
# Wed, 16 Aug 2023 06:16:20 GMT
WORKDIR /app/bundle
# Wed, 16 Aug 2023 06:16:20 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 16 Aug 2023 06:16:20 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 06:16:20 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba86ce7b915b9e4e83f102cd4770c615c732e908b35020d1254c9c2b4a2a4df`  
		Last Modified: Wed, 16 Aug 2023 06:19:59 GMT  
		Size: 35.7 MB (35734357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da655d17b01df1cc69609e9a4617a66c435ae2a1c6741d0058e781d34c43518`  
		Last Modified: Wed, 16 Aug 2023 06:19:54 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7135a46a6890a94c0e07f15d3de19b8c6ad727ddd6d63492c7f334bcfd7c83e`  
		Last Modified: Wed, 16 Aug 2023 06:20:38 GMT  
		Size: 257.3 MB (257273573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.2`

```console
$ docker pull rocket.chat@sha256:6ca35d031fade4fda98f573c2a0316f0af0794ecfed984e515aa2029c049fe2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.2` - linux; amd64

```console
$ docker pull rocket.chat@sha256:cf62a14ff9f8560dd651115e649782c90b7e958d9cdbed09e5b1a5c48458f071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313324585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f1370251c4ab299424648152544b6c6e44d0900b3ccd5fee4df6375b5c3e1c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_ENV=production
# Wed, 16 Aug 2023 06:16:25 GMT
ENV NODE_VERSION=14.21.2
# Wed, 16 Aug 2023 06:16:48 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 06:16:49 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 16 Aug 2023 06:16:49 GMT
VOLUME [/app/uploads]
# Wed, 16 Aug 2023 06:16:49 GMT
ENV RC_VERSION=6.2.12
# Wed, 16 Aug 2023 06:16:49 GMT
WORKDIR /app
# Wed, 16 Aug 2023 06:17:47 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 16 Aug 2023 06:17:51 GMT
USER rocketchat
# Wed, 16 Aug 2023 06:17:52 GMT
WORKDIR /app/bundle
# Wed, 16 Aug 2023 06:17:52 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 16 Aug 2023 06:17:52 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 06:17:52 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c23bf75f8565b663c861a8338c44fd89d9bcf4a319d1dd957e54db0bbc8fe5`  
		Last Modified: Wed, 16 Aug 2023 06:20:57 GMT  
		Size: 36.5 MB (36530749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555842bb9c75a5e6c5adc2ccab97095eaef01619b88f6bf08068909286c26ad0`  
		Last Modified: Wed, 16 Aug 2023 06:20:51 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533eabfca5156ef85fd55e975404869d686522bd52da1ccccf81be81bc09f922`  
		Last Modified: Wed, 16 Aug 2023 06:21:33 GMT  
		Size: 249.6 MB (249604600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.2.12`

```console
$ docker pull rocket.chat@sha256:6ca35d031fade4fda98f573c2a0316f0af0794ecfed984e515aa2029c049fe2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.2.12` - linux; amd64

```console
$ docker pull rocket.chat@sha256:cf62a14ff9f8560dd651115e649782c90b7e958d9cdbed09e5b1a5c48458f071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313324585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f1370251c4ab299424648152544b6c6e44d0900b3ccd5fee4df6375b5c3e1c`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_ENV=production
# Wed, 16 Aug 2023 06:16:25 GMT
ENV NODE_VERSION=14.21.2
# Wed, 16 Aug 2023 06:16:48 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 06:16:49 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 16 Aug 2023 06:16:49 GMT
VOLUME [/app/uploads]
# Wed, 16 Aug 2023 06:16:49 GMT
ENV RC_VERSION=6.2.12
# Wed, 16 Aug 2023 06:16:49 GMT
WORKDIR /app
# Wed, 16 Aug 2023 06:17:47 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 16 Aug 2023 06:17:51 GMT
USER rocketchat
# Wed, 16 Aug 2023 06:17:52 GMT
WORKDIR /app/bundle
# Wed, 16 Aug 2023 06:17:52 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 16 Aug 2023 06:17:52 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 06:17:52 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c23bf75f8565b663c861a8338c44fd89d9bcf4a319d1dd957e54db0bbc8fe5`  
		Last Modified: Wed, 16 Aug 2023 06:20:57 GMT  
		Size: 36.5 MB (36530749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555842bb9c75a5e6c5adc2ccab97095eaef01619b88f6bf08068909286c26ad0`  
		Last Modified: Wed, 16 Aug 2023 06:20:51 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533eabfca5156ef85fd55e975404869d686522bd52da1ccccf81be81bc09f922`  
		Last Modified: Wed, 16 Aug 2023 06:21:33 GMT  
		Size: 249.6 MB (249604600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.3`

```console
$ docker pull rocket.chat@sha256:5f440075fa770ece6fa4edddb6195c68c0a5db231f7cada19578d540af82cc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.3` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3ece8402f9d5bf2df2ed0d2aa55eba7650bf56b9daed09f6ccc0f98118905f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320197166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7787de131f1ec7cd252a34296f5c9a2f74bf6a1835fe3f35c79975b326907fa1`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_ENV=production
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_VERSION=14.21.3
# Wed, 16 Aug 2023 06:15:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 06:15:13 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 16 Aug 2023 06:15:13 GMT
VOLUME [/app/uploads]
# Wed, 16 Aug 2023 06:15:13 GMT
ENV RC_VERSION=6.3.1
# Wed, 16 Aug 2023 06:15:13 GMT
WORKDIR /app
# Wed, 16 Aug 2023 06:16:15 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 16 Aug 2023 06:16:20 GMT
USER rocketchat
# Wed, 16 Aug 2023 06:16:20 GMT
WORKDIR /app/bundle
# Wed, 16 Aug 2023 06:16:20 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 16 Aug 2023 06:16:20 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 06:16:20 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba86ce7b915b9e4e83f102cd4770c615c732e908b35020d1254c9c2b4a2a4df`  
		Last Modified: Wed, 16 Aug 2023 06:19:59 GMT  
		Size: 35.7 MB (35734357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da655d17b01df1cc69609e9a4617a66c435ae2a1c6741d0058e781d34c43518`  
		Last Modified: Wed, 16 Aug 2023 06:19:54 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7135a46a6890a94c0e07f15d3de19b8c6ad727ddd6d63492c7f334bcfd7c83e`  
		Last Modified: Wed, 16 Aug 2023 06:20:38 GMT  
		Size: 257.3 MB (257273573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:6.3.1`

```console
$ docker pull rocket.chat@sha256:5f440075fa770ece6fa4edddb6195c68c0a5db231f7cada19578d540af82cc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:6.3.1` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3ece8402f9d5bf2df2ed0d2aa55eba7650bf56b9daed09f6ccc0f98118905f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320197166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7787de131f1ec7cd252a34296f5c9a2f74bf6a1835fe3f35c79975b326907fa1`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_ENV=production
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_VERSION=14.21.3
# Wed, 16 Aug 2023 06:15:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 06:15:13 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 16 Aug 2023 06:15:13 GMT
VOLUME [/app/uploads]
# Wed, 16 Aug 2023 06:15:13 GMT
ENV RC_VERSION=6.3.1
# Wed, 16 Aug 2023 06:15:13 GMT
WORKDIR /app
# Wed, 16 Aug 2023 06:16:15 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 16 Aug 2023 06:16:20 GMT
USER rocketchat
# Wed, 16 Aug 2023 06:16:20 GMT
WORKDIR /app/bundle
# Wed, 16 Aug 2023 06:16:20 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 16 Aug 2023 06:16:20 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 06:16:20 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba86ce7b915b9e4e83f102cd4770c615c732e908b35020d1254c9c2b4a2a4df`  
		Last Modified: Wed, 16 Aug 2023 06:19:59 GMT  
		Size: 35.7 MB (35734357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da655d17b01df1cc69609e9a4617a66c435ae2a1c6741d0058e781d34c43518`  
		Last Modified: Wed, 16 Aug 2023 06:19:54 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7135a46a6890a94c0e07f15d3de19b8c6ad727ddd6d63492c7f334bcfd7c83e`  
		Last Modified: Wed, 16 Aug 2023 06:20:38 GMT  
		Size: 257.3 MB (257273573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:5f440075fa770ece6fa4edddb6195c68c0a5db231f7cada19578d540af82cc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

```console
$ docker pull rocket.chat@sha256:3ece8402f9d5bf2df2ed0d2aa55eba7650bf56b9daed09f6ccc0f98118905f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320197166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7787de131f1ec7cd252a34296f5c9a2f74bf6a1835fe3f35c79975b326907fa1`
-	Default Command: `["node","main.js"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_ENV=production
# Wed, 16 Aug 2023 06:14:46 GMT
ENV NODE_VERSION=14.21.3
# Wed, 16 Aug 2023 06:15:12 GMT
RUN ARCH="x64"   && set -eux   && apt-get update && apt-get install -y --no-install-recommends ca-certificates curl wget gnupg dirmngr xz-utils   && rm -rf /var/lib/apt/lists/*   && for key in   4ED778F539E3634C779C87C6D7062848A1AB005C   94AE36675C464D64BAFA68DD7434390BDBE9B9C5   74F12602B6F1C4E913FAA37AD3A89613643B6201   71DCFD284A79C3B38668286BC97EC7A07EDE3FC1   8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600   C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C   DD8F2338BAE7501E3DD5AC78C273792F7D83545D   A48C2BEE680E841632CD4E44F07496B3EB3C1762   108F52B48DB57BB0CC439B2997B01419BD92F80A   B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do   gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||   gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && apt-mark auto '.*' > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 16 Aug 2023 06:15:13 GMT
RUN groupadd -r rocketchat   && useradd -r -g rocketchat rocketchat   && mkdir -p /app/uploads   && chown rocketchat:rocketchat /app/uploads
# Wed, 16 Aug 2023 06:15:13 GMT
VOLUME [/app/uploads]
# Wed, 16 Aug 2023 06:15:13 GMT
ENV RC_VERSION=6.3.1
# Wed, 16 Aug 2023 06:15:13 GMT
WORKDIR /app
# Wed, 16 Aug 2023 06:16:15 GMT
RUN set -eux   && apt-get update   && apt-get install -y --no-install-recommends fontconfig   && aptMark="$(apt-mark showmanual)"   && apt-get install -y --no-install-recommends g++ make python ca-certificates curl gnupg   && rm -rf /var/lib/apt/lists/*   && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/download" -o rocket.chat.tgz   && curl -fSL "https://releases.rocket.chat/${RC_VERSION}/asc" -o rocket.chat.tgz.asc   && gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz   && tar zxf rocket.chat.tgz   && rm rocket.chat.tgz rocket.chat.tgz.asc   && cd bundle/programs/server   && npm install   && apt-mark auto '.*' > /dev/null   && apt-mark manual $aptMark > /dev/null   && find /usr/local -type f -executable -exec ldd '{}' ';'   | awk '/=>/ { print $(NF-1) }'   | sort -u   | xargs -r dpkg-query --search   | cut -d: -f1   | sort -u   | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && npm cache clear --force   && chown -R rocketchat:rocketchat /app
# Wed, 16 Aug 2023 06:16:20 GMT
USER rocketchat
# Wed, 16 Aug 2023 06:16:20 GMT
WORKDIR /app/bundle
# Wed, 16 Aug 2023 06:16:20 GMT
ENV DEPLOY_METHOD=docker-official MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 16 Aug 2023 06:16:20 GMT
EXPOSE 3000
# Wed, 16 Aug 2023 06:16:20 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba86ce7b915b9e4e83f102cd4770c615c732e908b35020d1254c9c2b4a2a4df`  
		Last Modified: Wed, 16 Aug 2023 06:19:59 GMT  
		Size: 35.7 MB (35734357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da655d17b01df1cc69609e9a4617a66c435ae2a1c6741d0058e781d34c43518`  
		Last Modified: Wed, 16 Aug 2023 06:19:54 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7135a46a6890a94c0e07f15d3de19b8c6ad727ddd6d63492c7f334bcfd7c83e`  
		Last Modified: Wed, 16 Aug 2023 06:20:38 GMT  
		Size: 257.3 MB (257273573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
