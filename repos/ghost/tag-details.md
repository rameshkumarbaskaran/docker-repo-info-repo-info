<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5.69`](#ghost569)
-	[`ghost:5.69-alpine`](#ghost569-alpine)
-	[`ghost:5.69.0`](#ghost5690)
-	[`ghost:5.69.0-alpine`](#ghost5690-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:5592f7cc64c2736cbc11e7b5ba8c4a260cfa3717f5a5e511cf2a2d57bad7f6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:5` - linux; amd64

```console
$ docker pull ghost@sha256:937d78eb0a678aba143a95fd994df37034b13e1815d95bd3bb176cd7c4466b1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191983695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36740855a01dac184ea9b64bbe21d91bd84bee13cda8ce75ee58a923975b8534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:08:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 16:26:32 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 16:26:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 16:26:57 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 16:27:09 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 16:27:09 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 16:27:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:27:10 GMT
CMD ["node"]
# Mon, 16 Oct 2023 16:51:55 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 16:52:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 16:52:06 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 16:52:06 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 16:52:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 16:54:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 16:54:03 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 16:54:03 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 16:54:03 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 16:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:54:03 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 16:54:03 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e37ba7d55cf627d7a515836792f8cbcae450b50ddacf7479423e96b99d75656`  
		Last Modified: Thu, 12 Oct 2023 00:15:23 GMT  
		Size: 4.2 KB (4187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002620df87aa0387e2265b1a0a8a4cf6bc3f390a34ddbef1651cd202ead062f8`  
		Last Modified: Mon, 16 Oct 2023 16:35:30 GMT  
		Size: 46.4 MB (46426623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30f6d630a337c355d08f613f7d6e86c38b8c3e4e8f24784aa4e99d597aa781b`  
		Last Modified: Mon, 16 Oct 2023 16:35:23 GMT  
		Size: 2.8 MB (2770727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72e258397901700c61a75bf99c66b41d306e5fd9080a6ac0c710026e94abf27`  
		Last Modified: Mon, 16 Oct 2023 16:35:23 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a330a83dc7a84b2f7f0bafef6e708e1b74e0ae74d419081f713dcd4154a17`  
		Last Modified: Mon, 16 Oct 2023 16:56:53 GMT  
		Size: 1.5 MB (1469905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9077330d689580cc1928b6364c9666be42038efde1e5504eb0d285823a93402c`  
		Last Modified: Mon, 16 Oct 2023 16:56:56 GMT  
		Size: 11.4 MB (11363818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068bf5111bf90fa03eda13cb2486cf61396d2e277ae00060a2c7ff066192028c`  
		Last Modified: Mon, 16 Oct 2023 16:57:11 GMT  
		Size: 98.5 MB (98529575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40081701b49d3a882ea186b0e95b148993d28342e63d86dff1e336c12ca9053`  
		Last Modified: Mon, 16 Oct 2023 16:56:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6adf4643e2ea2fca923d845bcb53fd858b7a972703ddaadfdda60e6a64bec30c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205206730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea49cc33999704af6f3a575329a775783d415b1b8178d6a936eaf10255c9e199`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 23:19:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 20:07:47 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 20:08:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 20:08:23 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 20:08:36 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 20:08:36 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 20:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:08:36 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:34:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 20:34:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 20:34:52 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:34:52 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:35:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:42:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:42:33 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:42:33 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:42:33 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 20:42:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:42:34 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:42:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c88fd62ab16546a4c895d6ad8f01a3dfe22d1a07fe074491f45ef80da25431`  
		Last Modified: Thu, 12 Oct 2023 00:24:46 GMT  
		Size: 4.2 KB (4171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a06f6ae103ebd030decce00a4cc8e32a19ef0f8ad0276914f835369507a723`  
		Last Modified: Mon, 16 Oct 2023 20:17:31 GMT  
		Size: 43.0 MB (43022548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8d5077827a14ee0d8965c56b27f5afe4981eb37430981b13aea6302839c84e`  
		Last Modified: Mon, 16 Oct 2023 20:17:23 GMT  
		Size: 2.8 MB (2760725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef44d15f789fb7c5f486026196e533df5be09b7ae5c775eba6f1ff24d7e8089d`  
		Last Modified: Mon, 16 Oct 2023 20:17:23 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e2b0913a8496be4fd9c970344fd197899227dbd2cb30a3790f96009d5f8624`  
		Last Modified: Mon, 16 Oct 2023 20:51:33 GMT  
		Size: 1.4 MB (1438454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba40f16ee45cf5955ea3604046098cbd15e5b6587f6f44ae10540cee6bb6e64`  
		Last Modified: Mon, 16 Oct 2023 20:51:40 GMT  
		Size: 11.4 MB (11364177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92412f18d48fff0e8a9c63a5058848a398133924ddb3e592d96b7a18d75d4e39`  
		Last Modified: Mon, 16 Oct 2023 20:52:12 GMT  
		Size: 120.0 MB (120036650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae8f99c87ebe0414c89160d74606acc5004a85f3b29cf1613a8e74467f62a2`  
		Last Modified: Mon, 16 Oct 2023 20:51:32 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d061370a7ed9577fa730a31b63af29de3af0929065d45fefe4ae2cf42f639bd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209234892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fdd52a2c90a1f101ecf18520b41cc2bf6b80322788a54d59eb648b4015af87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:40:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 18:40:47 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 18:41:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 18:41:10 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 18:41:20 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 18:41:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 18:41:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:41:21 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:11:55 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 19:12:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 19:12:06 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:12:06 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:12:28 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:18:46 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:18:46 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:18:46 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 19:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:18:46 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:18:46 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c0b58a4c2a0d10e68fc166330a6deedc851b3ac46fef98c8bbb7d9d4fc032c`  
		Last Modified: Thu, 12 Oct 2023 03:32:17 GMT  
		Size: 4.2 KB (4191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5bcae6c0230e5d06b9117aa2798d47e893dd47443e5217f7f8b182dfabd4a8`  
		Last Modified: Mon, 16 Oct 2023 18:49:35 GMT  
		Size: 46.5 MB (46516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d075541aab707d326dbaa35c19794a83ce389d115fbe5474101dd10af237e4b`  
		Last Modified: Mon, 16 Oct 2023 18:49:29 GMT  
		Size: 2.8 MB (2770668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1204d42b94792c6a46927ba64709a7e29dfd0bcdf0d44149fcb8d4f36fb0ca4`  
		Last Modified: Mon, 16 Oct 2023 18:49:29 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1c31c66d5c8e1c2fde8957ebc0bf09ce40bb8a086a5bed66ea2ced65693657`  
		Last Modified: Mon, 16 Oct 2023 19:26:19 GMT  
		Size: 1.4 MB (1402415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3600194007499e5a20997f869734637469035b34683de5c4749cf06f085c9ea`  
		Last Modified: Mon, 16 Oct 2023 19:26:22 GMT  
		Size: 11.4 MB (11363908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34aee59abe6842d523da00dadbed2a288ff9e6d418871275eeb109ef837f482`  
		Last Modified: Mon, 16 Oct 2023 19:26:59 GMT  
		Size: 117.1 MB (117112037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc23cf7641ab01d4964d24bd31e5252407ec65b41a7c5743cacf207e2ef28d`  
		Last Modified: Mon, 16 Oct 2023 19:26:19 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5` - linux; ppc64le

```console
$ docker pull ghost@sha256:4e69aba2bf77b98baf77e320ac58ba755bb8b0bbb307069642502dcfeac7ccbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205916586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fad4b5ee20e2fbb3f25e531acc6783725a217a57ccb9a846369d558041c192`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:53 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Wed, 11 Oct 2023 17:44:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 21:20:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 17:41:00 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 17:42:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 17:42:13 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 17:42:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 17:42:54 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 17:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 17:42:55 GMT
CMD ["node"]
# Mon, 16 Oct 2023 18:05:44 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 18:06:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 18:06:18 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 18:06:18 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 18:06:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 18:06:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 18:06:51 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 18:06:51 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 18:20:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 18:20:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 18:20:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 18:20:19 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 18:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:20:28 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 18:20:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea410cd4a5e719800e963888d39e95c3304f03c9b6274ca138e124cca600b1`  
		Last Modified: Wed, 11 Oct 2023 22:19:07 GMT  
		Size: 4.2 KB (4185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc596c427dd68b1259ccfe96dd02ae17e7c2322e199ae7ab0e11be036711d4a9`  
		Last Modified: Mon, 16 Oct 2023 17:50:15 GMT  
		Size: 48.5 MB (48548480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56751402a723c92fc764a54ad4a35bea6dc20b3f1aef689a134948a34829c50`  
		Last Modified: Mon, 16 Oct 2023 17:50:06 GMT  
		Size: 2.8 MB (2770826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809fd57bad8306838adc75d8c5fd3a928c6e777d7cfbc05b554384f3b6d07a7`  
		Last Modified: Mon, 16 Oct 2023 17:50:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c882a4939693aa1cedc553358ab0380431ee1f3fb957d22adfa47848f4a9094`  
		Last Modified: Mon, 16 Oct 2023 18:20:48 GMT  
		Size: 1.4 MB (1392744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90e1477a0d32c2f11bf1de5b8512520b19e9dfb1292762384cff02c32fef54`  
		Last Modified: Mon, 16 Oct 2023 18:20:51 GMT  
		Size: 11.4 MB (11365705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a586bf88d0b231f22a5e5121f3b7414a9195eb5f7b2e8eef3125c864abdf8a`  
		Last Modified: Mon, 16 Oct 2023 18:21:15 GMT  
		Size: 106.5 MB (106539929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897acd0eb7b9fe55672d658b56813bfd024312ffd0e0ebca4d16d5a60172ed7`  
		Last Modified: Mon, 16 Oct 2023 18:20:47 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:4000abe65c29881fb22442927bbbc18a9154762533c7fa8b6f8157875b3ba941
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198196985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ac4509b83f162b3a20d8e141d5a3c0fa438eaab2704243efa6b50881922595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:11:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 19:26:33 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:26:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 19:27:00 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:27:11 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 19:27:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:27:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:27:11 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:48:20 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 19:48:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 19:48:29 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:48:29 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:49:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:49:18 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:49:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:49:19 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:55:30 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:55:46 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:55:46 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:55:46 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 19:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:55:47 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:55:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1232a8d204040b3d9f8ce99e019405b6bc475472eb81c144dfad2dbe15237f97`  
		Last Modified: Thu, 12 Oct 2023 04:28:13 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed9e3be403a99840a356edb58b5817add20d87956629a24d8037a390b69891`  
		Last Modified: Mon, 16 Oct 2023 19:32:23 GMT  
		Size: 46.3 MB (46288457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3467ff7578bfab1ad4a9107dc35d1663bbdd0ac3c5ec66ce2aa21b3364e00d1`  
		Last Modified: Mon, 16 Oct 2023 19:32:15 GMT  
		Size: 2.8 MB (2771451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80606ed396e3b219a063868a03be8770c9f3ace0f5528c693eeeb422d8d9fc87`  
		Last Modified: Mon, 16 Oct 2023 19:32:15 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ad27a74dde3d5b45e18468ec98608732d2340fe547593713f074aafd22a8`  
		Last Modified: Mon, 16 Oct 2023 19:56:12 GMT  
		Size: 1.4 MB (1436034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4f903be8fbd39002d2fa421bbb5eeed433cc6358f08058741efd790e61eee3`  
		Last Modified: Mon, 16 Oct 2023 19:56:15 GMT  
		Size: 11.4 MB (11363693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bb59920a1f8634233d4b6370eb8dc3269c70f154b91fb8208588afef2f4cad`  
		Last Modified: Mon, 16 Oct 2023 19:56:32 GMT  
		Size: 106.7 MB (106675249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d81c3e8f50e4af366c889fd3d92aea6f358ac6987974de680010c6cca710c58`  
		Last Modified: Mon, 16 Oct 2023 19:56:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:73f1619e47551cfdd81ae6e2d179951a7083b1e3f1d12055faa580ed0329ea6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:01bfb3bb2b469969a6abce07e6d28bd722576dbff07334e9deede599e6df0dcc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162046385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8905904f7279079eafd012f08974777c420f8cd0e56b1bf19498822357a281`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 16:24:20 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 16:24:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 16:24:30 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 16:24:34 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 16:24:34 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 16:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:24:35 GMT
CMD ["node"]
# Mon, 16 Oct 2023 16:54:20 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 16:54:21 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 16:54:21 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 16:54:21 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 16:54:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 16:56:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 16:56:25 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 16:56:25 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 16:56:25 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 16:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:56:26 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 16:56:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033f54f0a5153baf8a5e40f815c7bbd9c27ad232b9efcd9ff87ea37b52e34b45`  
		Last Modified: Mon, 16 Oct 2023 16:32:59 GMT  
		Size: 47.9 MB (47882552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd229524656b7cc4fcfbd5c8fdc4a289f6289ab2ff8f51aa1281dead0be417`  
		Last Modified: Mon, 16 Oct 2023 16:32:52 GMT  
		Size: 2.3 MB (2342744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7bbada826e20aeaca8697ad1260b2c445ef2fc64180fdb5d241fc0cc2088ab`  
		Last Modified: Mon, 16 Oct 2023 16:32:52 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc9564647686a90e0c8abd5e279ce306318c321d05da54fff693504a19acaf`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 11.3 KB (11313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b4092a87622ce9a33c8ece18ce7b5427ad4de86d543bf2b99bdaa617f4684`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 857.7 KB (857732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcc6b768d949f8fe698871e18ff797a976210c28cd3a3f6d529b945c3fbb2e0`  
		Last Modified: Mon, 16 Oct 2023 16:57:30 GMT  
		Size: 11.4 MB (11363862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288f4022ec0c8d75572d56fb277ef32d2e5f945996f983da2ef177b3d811c07d`  
		Last Modified: Mon, 16 Oct 2023 16:57:45 GMT  
		Size: 96.2 MB (96208576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541a857a8bb4173584aa54ea0b22a84ab77f96dacea4ea34251a8f2367f3f553`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:b1fca6a94245a7cbdb3582b9ce19fc1d9178a67324fc0089ce089f2409ee9656
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167834934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15aeaef2ca61598182ed319d7386c4f5f1d6b3a8cd5ae55b4492fd25c70c59c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 18:38:03 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:14:14 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 19:14:15 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:14:23 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 19:14:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:14:24 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:14:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 20:14:35 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 20:14:35 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:14:35 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:15:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:26:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:26:23 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:26:23 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:26:23 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 20:26:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:26:23 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:26:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f415473d39909779a9ced4eb567865bb60bd8c4bd0a63d8cc070885988fe9dd`  
		Last Modified: Mon, 16 Oct 2023 19:58:33 GMT  
		Size: 46.6 MB (46604107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97978632cc851576f0cb7237ebfdcdcf729523a53bd29648a9db888a404e74ff`  
		Last Modified: Mon, 16 Oct 2023 19:58:21 GMT  
		Size: 2.3 MB (2333251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88acc3a37de25984709560c7b1c378e78d0e0d88e4af4955f0603baefca2fb1b`  
		Last Modified: Mon, 16 Oct 2023 19:58:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cb37582abdc30ac7e6422025f85da3db251ed3d992fe772ad465d284ab04d2`  
		Last Modified: Mon, 16 Oct 2023 20:26:33 GMT  
		Size: 11.5 KB (11482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1352921cd650024ee4d2b7a78a2a3a29320681217ec5af19eac875ba8bd7b6`  
		Last Modified: Mon, 16 Oct 2023 20:26:34 GMT  
		Size: 852.1 KB (852055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56eb4e71d8f5944b338f71835ba3d5f49297f1ba4b7c052aa6a04d5dbd58be`  
		Last Modified: Mon, 16 Oct 2023 20:26:37 GMT  
		Size: 11.4 MB (11369871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6243bf3bed6d9f8cc3bd02cc5385c279a427db697c79e7e01bd93bb31344edb`  
		Last Modified: Mon, 16 Oct 2023 20:27:00 GMT  
		Size: 103.6 MB (103550722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d538e944dce2e79d055494a7a15d7e36dc705930108f10b774df3b2efbb29e`  
		Last Modified: Mon, 16 Oct 2023 20:26:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:30fd89f37f4a389c1db61286b087662ba8149d5ebda4af097749a1ec97532455
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166760006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6c2e10a4f99672014e34d71c961c992241186d0e004f894a053286795e71d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:29 GMT
ADD file:7f36c30ba2b714d09a8650dba1545abdf892443dadbe9113b9a166b84ba7ac3f in / 
# Mon, 07 Aug 2023 19:57:29 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 18:46:32 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:28:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 19:28:16 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:28:25 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 19:28:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:28:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:28:26 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:42:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 20:42:49 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 20:42:49 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:42:49 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:43:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:51:10 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:51:14 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:51:14 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:51:14 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 20:51:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:51:14 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:51:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b82e4fd40279a40aa2eecd301fabb2dca254727cc09daa8d0caf69ac28c44af1`  
		Last Modified: Mon, 07 Aug 2023 19:58:08 GMT  
		Size: 2.9 MB (2869425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3586eebdb95577161ff16425f85eb8feba2c58c486c9460b012d7ec660d60cb`  
		Last Modified: Mon, 16 Oct 2023 20:14:54 GMT  
		Size: 46.1 MB (46120148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90067fee2ddb35cd44b2d22dbbbcc478ef2fce71bd4eb56b7b2cc998b6d05f79`  
		Last Modified: Mon, 16 Oct 2023 20:14:46 GMT  
		Size: 2.3 MB (2333227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbf104935b929e86d3a4aa6960b128643eb9abd9f5ca8cc98d3d43e32efd408`  
		Last Modified: Mon, 16 Oct 2023 20:14:45 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4f0fbc19f92f3a73ac44c207e4d0d358ad2e1d25b88617a09926b44c6bc3a9`  
		Last Modified: Mon, 16 Oct 2023 20:52:27 GMT  
		Size: 11.3 KB (11281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c377b31bf856bdd5320715b41552621eed54cc17b3e713cac5e558c919a449d`  
		Last Modified: Mon, 16 Oct 2023 20:52:27 GMT  
		Size: 781.9 KB (781860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1049d5f1e4eefb9d7138a0264b55d681e076e962183abca5245996cd0c97a231`  
		Last Modified: Mon, 16 Oct 2023 20:52:31 GMT  
		Size: 11.4 MB (11364177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dd375f004183a4d4524b7474a0d0f69d02841fb9fa76627092bfb99d78d405`  
		Last Modified: Mon, 16 Oct 2023 20:52:52 GMT  
		Size: 103.3 MB (103278894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341163b15ef28dd94a2af354bcf7a344c1b72d618837b73cc52f93d54cf08b95`  
		Last Modified: Mon, 16 Oct 2023 20:52:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:e7ff98a9f5e015ead631388c78eeab289d840ac7db81aaceaa8c40c90f8f6042
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181013595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1705e5c5897236c3cbd412643f6b898737292091d2127fddec9ccf4ffb3d17a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 17:56:18 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 18:17:51 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 18:17:52 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 18:17:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 18:17:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 18:17:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:17:56 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:18:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 19:18:50 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 19:18:50 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:18:50 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:19:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:26:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:26:07 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:26:07 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:26:07 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 19:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:26:08 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:26:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9eeebfedfff83c826fdc684aad595811a2e46c4a1b4fbf9c7d9b9d8413b6a5`  
		Last Modified: Mon, 16 Oct 2023 18:47:14 GMT  
		Size: 47.6 MB (47611982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf6c5ea44d1eedc0d68e6beecd63d0298b0fba3d586fcfb74ec9fdeb7f673fa`  
		Last Modified: Mon, 16 Oct 2023 18:47:08 GMT  
		Size: 2.3 MB (2342688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4afc6a2288f3616e27b1a3a04d90142c8670c80dc7156468262b95b58c0890f`  
		Last Modified: Mon, 16 Oct 2023 18:47:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66706788b67f9062b71f6f35d57f96cb85def5030722277f90d7102b7829dcb1`  
		Last Modified: Mon, 16 Oct 2023 19:27:18 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45738366bf6e97c1785529dc49baddfcabfb96f95c1fd25498973da41baa0769`  
		Last Modified: Mon, 16 Oct 2023 19:27:18 GMT  
		Size: 901.7 KB (901727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebed4246a56a80cb04d16e11fa0cea2f6330aac4f18545d75b3ac1fae5a66e25`  
		Last Modified: Mon, 16 Oct 2023 19:27:20 GMT  
		Size: 11.4 MB (11364034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0079e4ba77f8bcef7b95d45011f2eac18ddd60ce2134db6f289c699f9a2f7a`  
		Last Modified: Mon, 16 Oct 2023 19:27:35 GMT  
		Size: 115.5 MB (115522349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4db652e2ace0bccf6a3e8c23720e9c222a4194f366110b75d51f0cbf84b67a`  
		Last Modified: Mon, 16 Oct 2023 19:27:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5.69`

```console
$ docker pull ghost@sha256:5592f7cc64c2736cbc11e7b5ba8c4a260cfa3717f5a5e511cf2a2d57bad7f6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:5.69` - linux; amd64

```console
$ docker pull ghost@sha256:937d78eb0a678aba143a95fd994df37034b13e1815d95bd3bb176cd7c4466b1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191983695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36740855a01dac184ea9b64bbe21d91bd84bee13cda8ce75ee58a923975b8534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:08:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 16:26:32 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 16:26:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 16:26:57 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 16:27:09 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 16:27:09 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 16:27:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:27:10 GMT
CMD ["node"]
# Mon, 16 Oct 2023 16:51:55 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 16:52:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 16:52:06 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 16:52:06 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 16:52:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 16:54:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 16:54:03 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 16:54:03 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 16:54:03 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 16:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:54:03 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 16:54:03 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e37ba7d55cf627d7a515836792f8cbcae450b50ddacf7479423e96b99d75656`  
		Last Modified: Thu, 12 Oct 2023 00:15:23 GMT  
		Size: 4.2 KB (4187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002620df87aa0387e2265b1a0a8a4cf6bc3f390a34ddbef1651cd202ead062f8`  
		Last Modified: Mon, 16 Oct 2023 16:35:30 GMT  
		Size: 46.4 MB (46426623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30f6d630a337c355d08f613f7d6e86c38b8c3e4e8f24784aa4e99d597aa781b`  
		Last Modified: Mon, 16 Oct 2023 16:35:23 GMT  
		Size: 2.8 MB (2770727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72e258397901700c61a75bf99c66b41d306e5fd9080a6ac0c710026e94abf27`  
		Last Modified: Mon, 16 Oct 2023 16:35:23 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a330a83dc7a84b2f7f0bafef6e708e1b74e0ae74d419081f713dcd4154a17`  
		Last Modified: Mon, 16 Oct 2023 16:56:53 GMT  
		Size: 1.5 MB (1469905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9077330d689580cc1928b6364c9666be42038efde1e5504eb0d285823a93402c`  
		Last Modified: Mon, 16 Oct 2023 16:56:56 GMT  
		Size: 11.4 MB (11363818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068bf5111bf90fa03eda13cb2486cf61396d2e277ae00060a2c7ff066192028c`  
		Last Modified: Mon, 16 Oct 2023 16:57:11 GMT  
		Size: 98.5 MB (98529575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40081701b49d3a882ea186b0e95b148993d28342e63d86dff1e336c12ca9053`  
		Last Modified: Mon, 16 Oct 2023 16:56:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6adf4643e2ea2fca923d845bcb53fd858b7a972703ddaadfdda60e6a64bec30c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205206730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea49cc33999704af6f3a575329a775783d415b1b8178d6a936eaf10255c9e199`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 23:19:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 20:07:47 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 20:08:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 20:08:23 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 20:08:36 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 20:08:36 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 20:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:08:36 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:34:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 20:34:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 20:34:52 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:34:52 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:35:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:42:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:42:33 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:42:33 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:42:33 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 20:42:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:42:34 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:42:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c88fd62ab16546a4c895d6ad8f01a3dfe22d1a07fe074491f45ef80da25431`  
		Last Modified: Thu, 12 Oct 2023 00:24:46 GMT  
		Size: 4.2 KB (4171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a06f6ae103ebd030decce00a4cc8e32a19ef0f8ad0276914f835369507a723`  
		Last Modified: Mon, 16 Oct 2023 20:17:31 GMT  
		Size: 43.0 MB (43022548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8d5077827a14ee0d8965c56b27f5afe4981eb37430981b13aea6302839c84e`  
		Last Modified: Mon, 16 Oct 2023 20:17:23 GMT  
		Size: 2.8 MB (2760725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef44d15f789fb7c5f486026196e533df5be09b7ae5c775eba6f1ff24d7e8089d`  
		Last Modified: Mon, 16 Oct 2023 20:17:23 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e2b0913a8496be4fd9c970344fd197899227dbd2cb30a3790f96009d5f8624`  
		Last Modified: Mon, 16 Oct 2023 20:51:33 GMT  
		Size: 1.4 MB (1438454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba40f16ee45cf5955ea3604046098cbd15e5b6587f6f44ae10540cee6bb6e64`  
		Last Modified: Mon, 16 Oct 2023 20:51:40 GMT  
		Size: 11.4 MB (11364177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92412f18d48fff0e8a9c63a5058848a398133924ddb3e592d96b7a18d75d4e39`  
		Last Modified: Mon, 16 Oct 2023 20:52:12 GMT  
		Size: 120.0 MB (120036650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae8f99c87ebe0414c89160d74606acc5004a85f3b29cf1613a8e74467f62a2`  
		Last Modified: Mon, 16 Oct 2023 20:51:32 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d061370a7ed9577fa730a31b63af29de3af0929065d45fefe4ae2cf42f639bd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209234892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fdd52a2c90a1f101ecf18520b41cc2bf6b80322788a54d59eb648b4015af87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:40:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 18:40:47 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 18:41:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 18:41:10 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 18:41:20 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 18:41:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 18:41:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:41:21 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:11:55 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 19:12:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 19:12:06 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:12:06 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:12:28 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:18:46 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:18:46 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:18:46 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 19:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:18:46 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:18:46 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c0b58a4c2a0d10e68fc166330a6deedc851b3ac46fef98c8bbb7d9d4fc032c`  
		Last Modified: Thu, 12 Oct 2023 03:32:17 GMT  
		Size: 4.2 KB (4191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5bcae6c0230e5d06b9117aa2798d47e893dd47443e5217f7f8b182dfabd4a8`  
		Last Modified: Mon, 16 Oct 2023 18:49:35 GMT  
		Size: 46.5 MB (46516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d075541aab707d326dbaa35c19794a83ce389d115fbe5474101dd10af237e4b`  
		Last Modified: Mon, 16 Oct 2023 18:49:29 GMT  
		Size: 2.8 MB (2770668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1204d42b94792c6a46927ba64709a7e29dfd0bcdf0d44149fcb8d4f36fb0ca4`  
		Last Modified: Mon, 16 Oct 2023 18:49:29 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1c31c66d5c8e1c2fde8957ebc0bf09ce40bb8a086a5bed66ea2ced65693657`  
		Last Modified: Mon, 16 Oct 2023 19:26:19 GMT  
		Size: 1.4 MB (1402415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3600194007499e5a20997f869734637469035b34683de5c4749cf06f085c9ea`  
		Last Modified: Mon, 16 Oct 2023 19:26:22 GMT  
		Size: 11.4 MB (11363908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34aee59abe6842d523da00dadbed2a288ff9e6d418871275eeb109ef837f482`  
		Last Modified: Mon, 16 Oct 2023 19:26:59 GMT  
		Size: 117.1 MB (117112037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc23cf7641ab01d4964d24bd31e5252407ec65b41a7c5743cacf207e2ef28d`  
		Last Modified: Mon, 16 Oct 2023 19:26:19 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69` - linux; ppc64le

```console
$ docker pull ghost@sha256:4e69aba2bf77b98baf77e320ac58ba755bb8b0bbb307069642502dcfeac7ccbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205916586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fad4b5ee20e2fbb3f25e531acc6783725a217a57ccb9a846369d558041c192`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:53 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Wed, 11 Oct 2023 17:44:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 21:20:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 17:41:00 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 17:42:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 17:42:13 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 17:42:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 17:42:54 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 17:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 17:42:55 GMT
CMD ["node"]
# Mon, 16 Oct 2023 18:05:44 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 18:06:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 18:06:18 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 18:06:18 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 18:06:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 18:06:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 18:06:51 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 18:06:51 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 18:20:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 18:20:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 18:20:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 18:20:19 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 18:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:20:28 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 18:20:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea410cd4a5e719800e963888d39e95c3304f03c9b6274ca138e124cca600b1`  
		Last Modified: Wed, 11 Oct 2023 22:19:07 GMT  
		Size: 4.2 KB (4185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc596c427dd68b1259ccfe96dd02ae17e7c2322e199ae7ab0e11be036711d4a9`  
		Last Modified: Mon, 16 Oct 2023 17:50:15 GMT  
		Size: 48.5 MB (48548480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56751402a723c92fc764a54ad4a35bea6dc20b3f1aef689a134948a34829c50`  
		Last Modified: Mon, 16 Oct 2023 17:50:06 GMT  
		Size: 2.8 MB (2770826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809fd57bad8306838adc75d8c5fd3a928c6e777d7cfbc05b554384f3b6d07a7`  
		Last Modified: Mon, 16 Oct 2023 17:50:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c882a4939693aa1cedc553358ab0380431ee1f3fb957d22adfa47848f4a9094`  
		Last Modified: Mon, 16 Oct 2023 18:20:48 GMT  
		Size: 1.4 MB (1392744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90e1477a0d32c2f11bf1de5b8512520b19e9dfb1292762384cff02c32fef54`  
		Last Modified: Mon, 16 Oct 2023 18:20:51 GMT  
		Size: 11.4 MB (11365705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a586bf88d0b231f22a5e5121f3b7414a9195eb5f7b2e8eef3125c864abdf8a`  
		Last Modified: Mon, 16 Oct 2023 18:21:15 GMT  
		Size: 106.5 MB (106539929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897acd0eb7b9fe55672d658b56813bfd024312ffd0e0ebca4d16d5a60172ed7`  
		Last Modified: Mon, 16 Oct 2023 18:20:47 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69` - linux; s390x

```console
$ docker pull ghost@sha256:4000abe65c29881fb22442927bbbc18a9154762533c7fa8b6f8157875b3ba941
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198196985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ac4509b83f162b3a20d8e141d5a3c0fa438eaab2704243efa6b50881922595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:11:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 19:26:33 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:26:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 19:27:00 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:27:11 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 19:27:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:27:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:27:11 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:48:20 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 19:48:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 19:48:29 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:48:29 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:49:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:49:18 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:49:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:49:19 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:55:30 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:55:46 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:55:46 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:55:46 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 19:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:55:47 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:55:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1232a8d204040b3d9f8ce99e019405b6bc475472eb81c144dfad2dbe15237f97`  
		Last Modified: Thu, 12 Oct 2023 04:28:13 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed9e3be403a99840a356edb58b5817add20d87956629a24d8037a390b69891`  
		Last Modified: Mon, 16 Oct 2023 19:32:23 GMT  
		Size: 46.3 MB (46288457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3467ff7578bfab1ad4a9107dc35d1663bbdd0ac3c5ec66ce2aa21b3364e00d1`  
		Last Modified: Mon, 16 Oct 2023 19:32:15 GMT  
		Size: 2.8 MB (2771451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80606ed396e3b219a063868a03be8770c9f3ace0f5528c693eeeb422d8d9fc87`  
		Last Modified: Mon, 16 Oct 2023 19:32:15 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ad27a74dde3d5b45e18468ec98608732d2340fe547593713f074aafd22a8`  
		Last Modified: Mon, 16 Oct 2023 19:56:12 GMT  
		Size: 1.4 MB (1436034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4f903be8fbd39002d2fa421bbb5eeed433cc6358f08058741efd790e61eee3`  
		Last Modified: Mon, 16 Oct 2023 19:56:15 GMT  
		Size: 11.4 MB (11363693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bb59920a1f8634233d4b6370eb8dc3269c70f154b91fb8208588afef2f4cad`  
		Last Modified: Mon, 16 Oct 2023 19:56:32 GMT  
		Size: 106.7 MB (106675249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d81c3e8f50e4af366c889fd3d92aea6f358ac6987974de680010c6cca710c58`  
		Last Modified: Mon, 16 Oct 2023 19:56:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5.69-alpine`

```console
$ docker pull ghost@sha256:73f1619e47551cfdd81ae6e2d179951a7083b1e3f1d12055faa580ed0329ea6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:5.69-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:01bfb3bb2b469969a6abce07e6d28bd722576dbff07334e9deede599e6df0dcc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162046385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8905904f7279079eafd012f08974777c420f8cd0e56b1bf19498822357a281`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 16:24:20 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 16:24:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 16:24:30 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 16:24:34 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 16:24:34 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 16:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:24:35 GMT
CMD ["node"]
# Mon, 16 Oct 2023 16:54:20 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 16:54:21 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 16:54:21 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 16:54:21 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 16:54:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 16:56:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 16:56:25 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 16:56:25 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 16:56:25 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 16:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:56:26 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 16:56:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033f54f0a5153baf8a5e40f815c7bbd9c27ad232b9efcd9ff87ea37b52e34b45`  
		Last Modified: Mon, 16 Oct 2023 16:32:59 GMT  
		Size: 47.9 MB (47882552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd229524656b7cc4fcfbd5c8fdc4a289f6289ab2ff8f51aa1281dead0be417`  
		Last Modified: Mon, 16 Oct 2023 16:32:52 GMT  
		Size: 2.3 MB (2342744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7bbada826e20aeaca8697ad1260b2c445ef2fc64180fdb5d241fc0cc2088ab`  
		Last Modified: Mon, 16 Oct 2023 16:32:52 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc9564647686a90e0c8abd5e279ce306318c321d05da54fff693504a19acaf`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 11.3 KB (11313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b4092a87622ce9a33c8ece18ce7b5427ad4de86d543bf2b99bdaa617f4684`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 857.7 KB (857732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcc6b768d949f8fe698871e18ff797a976210c28cd3a3f6d529b945c3fbb2e0`  
		Last Modified: Mon, 16 Oct 2023 16:57:30 GMT  
		Size: 11.4 MB (11363862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288f4022ec0c8d75572d56fb277ef32d2e5f945996f983da2ef177b3d811c07d`  
		Last Modified: Mon, 16 Oct 2023 16:57:45 GMT  
		Size: 96.2 MB (96208576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541a857a8bb4173584aa54ea0b22a84ab77f96dacea4ea34251a8f2367f3f553`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:b1fca6a94245a7cbdb3582b9ce19fc1d9178a67324fc0089ce089f2409ee9656
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167834934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15aeaef2ca61598182ed319d7386c4f5f1d6b3a8cd5ae55b4492fd25c70c59c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 18:38:03 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:14:14 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 19:14:15 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:14:23 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 19:14:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:14:24 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:14:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 20:14:35 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 20:14:35 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:14:35 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:15:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:26:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:26:23 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:26:23 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:26:23 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 20:26:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:26:23 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:26:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f415473d39909779a9ced4eb567865bb60bd8c4bd0a63d8cc070885988fe9dd`  
		Last Modified: Mon, 16 Oct 2023 19:58:33 GMT  
		Size: 46.6 MB (46604107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97978632cc851576f0cb7237ebfdcdcf729523a53bd29648a9db888a404e74ff`  
		Last Modified: Mon, 16 Oct 2023 19:58:21 GMT  
		Size: 2.3 MB (2333251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88acc3a37de25984709560c7b1c378e78d0e0d88e4af4955f0603baefca2fb1b`  
		Last Modified: Mon, 16 Oct 2023 19:58:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cb37582abdc30ac7e6422025f85da3db251ed3d992fe772ad465d284ab04d2`  
		Last Modified: Mon, 16 Oct 2023 20:26:33 GMT  
		Size: 11.5 KB (11482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1352921cd650024ee4d2b7a78a2a3a29320681217ec5af19eac875ba8bd7b6`  
		Last Modified: Mon, 16 Oct 2023 20:26:34 GMT  
		Size: 852.1 KB (852055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56eb4e71d8f5944b338f71835ba3d5f49297f1ba4b7c052aa6a04d5dbd58be`  
		Last Modified: Mon, 16 Oct 2023 20:26:37 GMT  
		Size: 11.4 MB (11369871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6243bf3bed6d9f8cc3bd02cc5385c279a427db697c79e7e01bd93bb31344edb`  
		Last Modified: Mon, 16 Oct 2023 20:27:00 GMT  
		Size: 103.6 MB (103550722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d538e944dce2e79d055494a7a15d7e36dc705930108f10b774df3b2efbb29e`  
		Last Modified: Mon, 16 Oct 2023 20:26:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:30fd89f37f4a389c1db61286b087662ba8149d5ebda4af097749a1ec97532455
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166760006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6c2e10a4f99672014e34d71c961c992241186d0e004f894a053286795e71d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:29 GMT
ADD file:7f36c30ba2b714d09a8650dba1545abdf892443dadbe9113b9a166b84ba7ac3f in / 
# Mon, 07 Aug 2023 19:57:29 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 18:46:32 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:28:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 19:28:16 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:28:25 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 19:28:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:28:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:28:26 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:42:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 20:42:49 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 20:42:49 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:42:49 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:43:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:51:10 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:51:14 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:51:14 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:51:14 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 20:51:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:51:14 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:51:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b82e4fd40279a40aa2eecd301fabb2dca254727cc09daa8d0caf69ac28c44af1`  
		Last Modified: Mon, 07 Aug 2023 19:58:08 GMT  
		Size: 2.9 MB (2869425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3586eebdb95577161ff16425f85eb8feba2c58c486c9460b012d7ec660d60cb`  
		Last Modified: Mon, 16 Oct 2023 20:14:54 GMT  
		Size: 46.1 MB (46120148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90067fee2ddb35cd44b2d22dbbbcc478ef2fce71bd4eb56b7b2cc998b6d05f79`  
		Last Modified: Mon, 16 Oct 2023 20:14:46 GMT  
		Size: 2.3 MB (2333227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbf104935b929e86d3a4aa6960b128643eb9abd9f5ca8cc98d3d43e32efd408`  
		Last Modified: Mon, 16 Oct 2023 20:14:45 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4f0fbc19f92f3a73ac44c207e4d0d358ad2e1d25b88617a09926b44c6bc3a9`  
		Last Modified: Mon, 16 Oct 2023 20:52:27 GMT  
		Size: 11.3 KB (11281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c377b31bf856bdd5320715b41552621eed54cc17b3e713cac5e558c919a449d`  
		Last Modified: Mon, 16 Oct 2023 20:52:27 GMT  
		Size: 781.9 KB (781860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1049d5f1e4eefb9d7138a0264b55d681e076e962183abca5245996cd0c97a231`  
		Last Modified: Mon, 16 Oct 2023 20:52:31 GMT  
		Size: 11.4 MB (11364177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dd375f004183a4d4524b7474a0d0f69d02841fb9fa76627092bfb99d78d405`  
		Last Modified: Mon, 16 Oct 2023 20:52:52 GMT  
		Size: 103.3 MB (103278894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341163b15ef28dd94a2af354bcf7a344c1b72d618837b73cc52f93d54cf08b95`  
		Last Modified: Mon, 16 Oct 2023 20:52:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:e7ff98a9f5e015ead631388c78eeab289d840ac7db81aaceaa8c40c90f8f6042
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181013595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1705e5c5897236c3cbd412643f6b898737292091d2127fddec9ccf4ffb3d17a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 17:56:18 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 18:17:51 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 18:17:52 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 18:17:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 18:17:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 18:17:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:17:56 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:18:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 19:18:50 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 19:18:50 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:18:50 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:19:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:26:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:26:07 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:26:07 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:26:07 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 19:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:26:08 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:26:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9eeebfedfff83c826fdc684aad595811a2e46c4a1b4fbf9c7d9b9d8413b6a5`  
		Last Modified: Mon, 16 Oct 2023 18:47:14 GMT  
		Size: 47.6 MB (47611982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf6c5ea44d1eedc0d68e6beecd63d0298b0fba3d586fcfb74ec9fdeb7f673fa`  
		Last Modified: Mon, 16 Oct 2023 18:47:08 GMT  
		Size: 2.3 MB (2342688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4afc6a2288f3616e27b1a3a04d90142c8670c80dc7156468262b95b58c0890f`  
		Last Modified: Mon, 16 Oct 2023 18:47:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66706788b67f9062b71f6f35d57f96cb85def5030722277f90d7102b7829dcb1`  
		Last Modified: Mon, 16 Oct 2023 19:27:18 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45738366bf6e97c1785529dc49baddfcabfb96f95c1fd25498973da41baa0769`  
		Last Modified: Mon, 16 Oct 2023 19:27:18 GMT  
		Size: 901.7 KB (901727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebed4246a56a80cb04d16e11fa0cea2f6330aac4f18545d75b3ac1fae5a66e25`  
		Last Modified: Mon, 16 Oct 2023 19:27:20 GMT  
		Size: 11.4 MB (11364034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0079e4ba77f8bcef7b95d45011f2eac18ddd60ce2134db6f289c699f9a2f7a`  
		Last Modified: Mon, 16 Oct 2023 19:27:35 GMT  
		Size: 115.5 MB (115522349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4db652e2ace0bccf6a3e8c23720e9c222a4194f366110b75d51f0cbf84b67a`  
		Last Modified: Mon, 16 Oct 2023 19:27:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5.69.0`

```console
$ docker pull ghost@sha256:5592f7cc64c2736cbc11e7b5ba8c4a260cfa3717f5a5e511cf2a2d57bad7f6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:5.69.0` - linux; amd64

```console
$ docker pull ghost@sha256:937d78eb0a678aba143a95fd994df37034b13e1815d95bd3bb176cd7c4466b1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191983695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36740855a01dac184ea9b64bbe21d91bd84bee13cda8ce75ee58a923975b8534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:08:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 16:26:32 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 16:26:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 16:26:57 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 16:27:09 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 16:27:09 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 16:27:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:27:10 GMT
CMD ["node"]
# Mon, 16 Oct 2023 16:51:55 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 16:52:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 16:52:06 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 16:52:06 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 16:52:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 16:54:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 16:54:03 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 16:54:03 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 16:54:03 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 16:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:54:03 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 16:54:03 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e37ba7d55cf627d7a515836792f8cbcae450b50ddacf7479423e96b99d75656`  
		Last Modified: Thu, 12 Oct 2023 00:15:23 GMT  
		Size: 4.2 KB (4187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002620df87aa0387e2265b1a0a8a4cf6bc3f390a34ddbef1651cd202ead062f8`  
		Last Modified: Mon, 16 Oct 2023 16:35:30 GMT  
		Size: 46.4 MB (46426623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30f6d630a337c355d08f613f7d6e86c38b8c3e4e8f24784aa4e99d597aa781b`  
		Last Modified: Mon, 16 Oct 2023 16:35:23 GMT  
		Size: 2.8 MB (2770727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72e258397901700c61a75bf99c66b41d306e5fd9080a6ac0c710026e94abf27`  
		Last Modified: Mon, 16 Oct 2023 16:35:23 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a330a83dc7a84b2f7f0bafef6e708e1b74e0ae74d419081f713dcd4154a17`  
		Last Modified: Mon, 16 Oct 2023 16:56:53 GMT  
		Size: 1.5 MB (1469905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9077330d689580cc1928b6364c9666be42038efde1e5504eb0d285823a93402c`  
		Last Modified: Mon, 16 Oct 2023 16:56:56 GMT  
		Size: 11.4 MB (11363818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068bf5111bf90fa03eda13cb2486cf61396d2e277ae00060a2c7ff066192028c`  
		Last Modified: Mon, 16 Oct 2023 16:57:11 GMT  
		Size: 98.5 MB (98529575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40081701b49d3a882ea186b0e95b148993d28342e63d86dff1e336c12ca9053`  
		Last Modified: Mon, 16 Oct 2023 16:56:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6adf4643e2ea2fca923d845bcb53fd858b7a972703ddaadfdda60e6a64bec30c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205206730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea49cc33999704af6f3a575329a775783d415b1b8178d6a936eaf10255c9e199`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 23:19:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 20:07:47 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 20:08:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 20:08:23 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 20:08:36 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 20:08:36 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 20:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:08:36 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:34:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 20:34:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 20:34:52 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:34:52 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:35:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:42:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:42:33 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:42:33 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:42:33 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 20:42:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:42:34 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:42:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c88fd62ab16546a4c895d6ad8f01a3dfe22d1a07fe074491f45ef80da25431`  
		Last Modified: Thu, 12 Oct 2023 00:24:46 GMT  
		Size: 4.2 KB (4171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a06f6ae103ebd030decce00a4cc8e32a19ef0f8ad0276914f835369507a723`  
		Last Modified: Mon, 16 Oct 2023 20:17:31 GMT  
		Size: 43.0 MB (43022548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8d5077827a14ee0d8965c56b27f5afe4981eb37430981b13aea6302839c84e`  
		Last Modified: Mon, 16 Oct 2023 20:17:23 GMT  
		Size: 2.8 MB (2760725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef44d15f789fb7c5f486026196e533df5be09b7ae5c775eba6f1ff24d7e8089d`  
		Last Modified: Mon, 16 Oct 2023 20:17:23 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e2b0913a8496be4fd9c970344fd197899227dbd2cb30a3790f96009d5f8624`  
		Last Modified: Mon, 16 Oct 2023 20:51:33 GMT  
		Size: 1.4 MB (1438454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba40f16ee45cf5955ea3604046098cbd15e5b6587f6f44ae10540cee6bb6e64`  
		Last Modified: Mon, 16 Oct 2023 20:51:40 GMT  
		Size: 11.4 MB (11364177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92412f18d48fff0e8a9c63a5058848a398133924ddb3e592d96b7a18d75d4e39`  
		Last Modified: Mon, 16 Oct 2023 20:52:12 GMT  
		Size: 120.0 MB (120036650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae8f99c87ebe0414c89160d74606acc5004a85f3b29cf1613a8e74467f62a2`  
		Last Modified: Mon, 16 Oct 2023 20:51:32 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d061370a7ed9577fa730a31b63af29de3af0929065d45fefe4ae2cf42f639bd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209234892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fdd52a2c90a1f101ecf18520b41cc2bf6b80322788a54d59eb648b4015af87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:40:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 18:40:47 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 18:41:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 18:41:10 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 18:41:20 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 18:41:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 18:41:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:41:21 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:11:55 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 19:12:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 19:12:06 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:12:06 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:12:28 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:18:46 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:18:46 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:18:46 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 19:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:18:46 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:18:46 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c0b58a4c2a0d10e68fc166330a6deedc851b3ac46fef98c8bbb7d9d4fc032c`  
		Last Modified: Thu, 12 Oct 2023 03:32:17 GMT  
		Size: 4.2 KB (4191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5bcae6c0230e5d06b9117aa2798d47e893dd47443e5217f7f8b182dfabd4a8`  
		Last Modified: Mon, 16 Oct 2023 18:49:35 GMT  
		Size: 46.5 MB (46516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d075541aab707d326dbaa35c19794a83ce389d115fbe5474101dd10af237e4b`  
		Last Modified: Mon, 16 Oct 2023 18:49:29 GMT  
		Size: 2.8 MB (2770668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1204d42b94792c6a46927ba64709a7e29dfd0bcdf0d44149fcb8d4f36fb0ca4`  
		Last Modified: Mon, 16 Oct 2023 18:49:29 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1c31c66d5c8e1c2fde8957ebc0bf09ce40bb8a086a5bed66ea2ced65693657`  
		Last Modified: Mon, 16 Oct 2023 19:26:19 GMT  
		Size: 1.4 MB (1402415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3600194007499e5a20997f869734637469035b34683de5c4749cf06f085c9ea`  
		Last Modified: Mon, 16 Oct 2023 19:26:22 GMT  
		Size: 11.4 MB (11363908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34aee59abe6842d523da00dadbed2a288ff9e6d418871275eeb109ef837f482`  
		Last Modified: Mon, 16 Oct 2023 19:26:59 GMT  
		Size: 117.1 MB (117112037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc23cf7641ab01d4964d24bd31e5252407ec65b41a7c5743cacf207e2ef28d`  
		Last Modified: Mon, 16 Oct 2023 19:26:19 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69.0` - linux; ppc64le

```console
$ docker pull ghost@sha256:4e69aba2bf77b98baf77e320ac58ba755bb8b0bbb307069642502dcfeac7ccbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205916586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fad4b5ee20e2fbb3f25e531acc6783725a217a57ccb9a846369d558041c192`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:53 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Wed, 11 Oct 2023 17:44:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 21:20:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 17:41:00 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 17:42:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 17:42:13 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 17:42:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 17:42:54 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 17:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 17:42:55 GMT
CMD ["node"]
# Mon, 16 Oct 2023 18:05:44 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 18:06:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 18:06:18 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 18:06:18 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 18:06:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 18:06:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 18:06:51 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 18:06:51 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 18:20:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 18:20:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 18:20:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 18:20:19 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 18:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:20:28 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 18:20:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea410cd4a5e719800e963888d39e95c3304f03c9b6274ca138e124cca600b1`  
		Last Modified: Wed, 11 Oct 2023 22:19:07 GMT  
		Size: 4.2 KB (4185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc596c427dd68b1259ccfe96dd02ae17e7c2322e199ae7ab0e11be036711d4a9`  
		Last Modified: Mon, 16 Oct 2023 17:50:15 GMT  
		Size: 48.5 MB (48548480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56751402a723c92fc764a54ad4a35bea6dc20b3f1aef689a134948a34829c50`  
		Last Modified: Mon, 16 Oct 2023 17:50:06 GMT  
		Size: 2.8 MB (2770826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809fd57bad8306838adc75d8c5fd3a928c6e777d7cfbc05b554384f3b6d07a7`  
		Last Modified: Mon, 16 Oct 2023 17:50:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c882a4939693aa1cedc553358ab0380431ee1f3fb957d22adfa47848f4a9094`  
		Last Modified: Mon, 16 Oct 2023 18:20:48 GMT  
		Size: 1.4 MB (1392744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90e1477a0d32c2f11bf1de5b8512520b19e9dfb1292762384cff02c32fef54`  
		Last Modified: Mon, 16 Oct 2023 18:20:51 GMT  
		Size: 11.4 MB (11365705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a586bf88d0b231f22a5e5121f3b7414a9195eb5f7b2e8eef3125c864abdf8a`  
		Last Modified: Mon, 16 Oct 2023 18:21:15 GMT  
		Size: 106.5 MB (106539929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897acd0eb7b9fe55672d658b56813bfd024312ffd0e0ebca4d16d5a60172ed7`  
		Last Modified: Mon, 16 Oct 2023 18:20:47 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69.0` - linux; s390x

```console
$ docker pull ghost@sha256:4000abe65c29881fb22442927bbbc18a9154762533c7fa8b6f8157875b3ba941
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198196985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ac4509b83f162b3a20d8e141d5a3c0fa438eaab2704243efa6b50881922595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:11:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 19:26:33 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:26:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 19:27:00 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:27:11 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 19:27:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:27:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:27:11 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:48:20 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 19:48:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 19:48:29 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:48:29 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:49:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:49:18 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:49:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:49:19 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:55:30 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:55:46 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:55:46 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:55:46 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 19:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:55:47 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:55:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1232a8d204040b3d9f8ce99e019405b6bc475472eb81c144dfad2dbe15237f97`  
		Last Modified: Thu, 12 Oct 2023 04:28:13 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed9e3be403a99840a356edb58b5817add20d87956629a24d8037a390b69891`  
		Last Modified: Mon, 16 Oct 2023 19:32:23 GMT  
		Size: 46.3 MB (46288457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3467ff7578bfab1ad4a9107dc35d1663bbdd0ac3c5ec66ce2aa21b3364e00d1`  
		Last Modified: Mon, 16 Oct 2023 19:32:15 GMT  
		Size: 2.8 MB (2771451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80606ed396e3b219a063868a03be8770c9f3ace0f5528c693eeeb422d8d9fc87`  
		Last Modified: Mon, 16 Oct 2023 19:32:15 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ad27a74dde3d5b45e18468ec98608732d2340fe547593713f074aafd22a8`  
		Last Modified: Mon, 16 Oct 2023 19:56:12 GMT  
		Size: 1.4 MB (1436034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4f903be8fbd39002d2fa421bbb5eeed433cc6358f08058741efd790e61eee3`  
		Last Modified: Mon, 16 Oct 2023 19:56:15 GMT  
		Size: 11.4 MB (11363693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bb59920a1f8634233d4b6370eb8dc3269c70f154b91fb8208588afef2f4cad`  
		Last Modified: Mon, 16 Oct 2023 19:56:32 GMT  
		Size: 106.7 MB (106675249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d81c3e8f50e4af366c889fd3d92aea6f358ac6987974de680010c6cca710c58`  
		Last Modified: Mon, 16 Oct 2023 19:56:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:5.69.0-alpine`

```console
$ docker pull ghost@sha256:73f1619e47551cfdd81ae6e2d179951a7083b1e3f1d12055faa580ed0329ea6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:5.69.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:01bfb3bb2b469969a6abce07e6d28bd722576dbff07334e9deede599e6df0dcc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162046385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8905904f7279079eafd012f08974777c420f8cd0e56b1bf19498822357a281`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 16:24:20 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 16:24:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 16:24:30 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 16:24:34 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 16:24:34 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 16:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:24:35 GMT
CMD ["node"]
# Mon, 16 Oct 2023 16:54:20 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 16:54:21 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 16:54:21 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 16:54:21 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 16:54:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 16:56:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 16:56:25 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 16:56:25 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 16:56:25 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 16:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:56:26 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 16:56:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033f54f0a5153baf8a5e40f815c7bbd9c27ad232b9efcd9ff87ea37b52e34b45`  
		Last Modified: Mon, 16 Oct 2023 16:32:59 GMT  
		Size: 47.9 MB (47882552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd229524656b7cc4fcfbd5c8fdc4a289f6289ab2ff8f51aa1281dead0be417`  
		Last Modified: Mon, 16 Oct 2023 16:32:52 GMT  
		Size: 2.3 MB (2342744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7bbada826e20aeaca8697ad1260b2c445ef2fc64180fdb5d241fc0cc2088ab`  
		Last Modified: Mon, 16 Oct 2023 16:32:52 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc9564647686a90e0c8abd5e279ce306318c321d05da54fff693504a19acaf`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 11.3 KB (11313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b4092a87622ce9a33c8ece18ce7b5427ad4de86d543bf2b99bdaa617f4684`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 857.7 KB (857732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcc6b768d949f8fe698871e18ff797a976210c28cd3a3f6d529b945c3fbb2e0`  
		Last Modified: Mon, 16 Oct 2023 16:57:30 GMT  
		Size: 11.4 MB (11363862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288f4022ec0c8d75572d56fb277ef32d2e5f945996f983da2ef177b3d811c07d`  
		Last Modified: Mon, 16 Oct 2023 16:57:45 GMT  
		Size: 96.2 MB (96208576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541a857a8bb4173584aa54ea0b22a84ab77f96dacea4ea34251a8f2367f3f553`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69.0-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:b1fca6a94245a7cbdb3582b9ce19fc1d9178a67324fc0089ce089f2409ee9656
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167834934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15aeaef2ca61598182ed319d7386c4f5f1d6b3a8cd5ae55b4492fd25c70c59c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 18:38:03 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:14:14 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 19:14:15 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:14:23 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 19:14:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:14:24 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:14:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 20:14:35 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 20:14:35 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:14:35 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:15:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:26:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:26:23 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:26:23 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:26:23 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 20:26:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:26:23 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:26:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f415473d39909779a9ced4eb567865bb60bd8c4bd0a63d8cc070885988fe9dd`  
		Last Modified: Mon, 16 Oct 2023 19:58:33 GMT  
		Size: 46.6 MB (46604107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97978632cc851576f0cb7237ebfdcdcf729523a53bd29648a9db888a404e74ff`  
		Last Modified: Mon, 16 Oct 2023 19:58:21 GMT  
		Size: 2.3 MB (2333251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88acc3a37de25984709560c7b1c378e78d0e0d88e4af4955f0603baefca2fb1b`  
		Last Modified: Mon, 16 Oct 2023 19:58:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cb37582abdc30ac7e6422025f85da3db251ed3d992fe772ad465d284ab04d2`  
		Last Modified: Mon, 16 Oct 2023 20:26:33 GMT  
		Size: 11.5 KB (11482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1352921cd650024ee4d2b7a78a2a3a29320681217ec5af19eac875ba8bd7b6`  
		Last Modified: Mon, 16 Oct 2023 20:26:34 GMT  
		Size: 852.1 KB (852055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56eb4e71d8f5944b338f71835ba3d5f49297f1ba4b7c052aa6a04d5dbd58be`  
		Last Modified: Mon, 16 Oct 2023 20:26:37 GMT  
		Size: 11.4 MB (11369871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6243bf3bed6d9f8cc3bd02cc5385c279a427db697c79e7e01bd93bb31344edb`  
		Last Modified: Mon, 16 Oct 2023 20:27:00 GMT  
		Size: 103.6 MB (103550722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d538e944dce2e79d055494a7a15d7e36dc705930108f10b774df3b2efbb29e`  
		Last Modified: Mon, 16 Oct 2023 20:26:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69.0-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:30fd89f37f4a389c1db61286b087662ba8149d5ebda4af097749a1ec97532455
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166760006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6c2e10a4f99672014e34d71c961c992241186d0e004f894a053286795e71d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:29 GMT
ADD file:7f36c30ba2b714d09a8650dba1545abdf892443dadbe9113b9a166b84ba7ac3f in / 
# Mon, 07 Aug 2023 19:57:29 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 18:46:32 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:28:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 19:28:16 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:28:25 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 19:28:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:28:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:28:26 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:42:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 20:42:49 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 20:42:49 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:42:49 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:43:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:51:10 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:51:14 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:51:14 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:51:14 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 20:51:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:51:14 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:51:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b82e4fd40279a40aa2eecd301fabb2dca254727cc09daa8d0caf69ac28c44af1`  
		Last Modified: Mon, 07 Aug 2023 19:58:08 GMT  
		Size: 2.9 MB (2869425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3586eebdb95577161ff16425f85eb8feba2c58c486c9460b012d7ec660d60cb`  
		Last Modified: Mon, 16 Oct 2023 20:14:54 GMT  
		Size: 46.1 MB (46120148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90067fee2ddb35cd44b2d22dbbbcc478ef2fce71bd4eb56b7b2cc998b6d05f79`  
		Last Modified: Mon, 16 Oct 2023 20:14:46 GMT  
		Size: 2.3 MB (2333227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbf104935b929e86d3a4aa6960b128643eb9abd9f5ca8cc98d3d43e32efd408`  
		Last Modified: Mon, 16 Oct 2023 20:14:45 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4f0fbc19f92f3a73ac44c207e4d0d358ad2e1d25b88617a09926b44c6bc3a9`  
		Last Modified: Mon, 16 Oct 2023 20:52:27 GMT  
		Size: 11.3 KB (11281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c377b31bf856bdd5320715b41552621eed54cc17b3e713cac5e558c919a449d`  
		Last Modified: Mon, 16 Oct 2023 20:52:27 GMT  
		Size: 781.9 KB (781860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1049d5f1e4eefb9d7138a0264b55d681e076e962183abca5245996cd0c97a231`  
		Last Modified: Mon, 16 Oct 2023 20:52:31 GMT  
		Size: 11.4 MB (11364177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dd375f004183a4d4524b7474a0d0f69d02841fb9fa76627092bfb99d78d405`  
		Last Modified: Mon, 16 Oct 2023 20:52:52 GMT  
		Size: 103.3 MB (103278894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341163b15ef28dd94a2af354bcf7a344c1b72d618837b73cc52f93d54cf08b95`  
		Last Modified: Mon, 16 Oct 2023 20:52:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:5.69.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:e7ff98a9f5e015ead631388c78eeab289d840ac7db81aaceaa8c40c90f8f6042
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181013595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1705e5c5897236c3cbd412643f6b898737292091d2127fddec9ccf4ffb3d17a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 17:56:18 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 18:17:51 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 18:17:52 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 18:17:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 18:17:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 18:17:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:17:56 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:18:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 19:18:50 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 19:18:50 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:18:50 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:19:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:26:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:26:07 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:26:07 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:26:07 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 19:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:26:08 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:26:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9eeebfedfff83c826fdc684aad595811a2e46c4a1b4fbf9c7d9b9d8413b6a5`  
		Last Modified: Mon, 16 Oct 2023 18:47:14 GMT  
		Size: 47.6 MB (47611982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf6c5ea44d1eedc0d68e6beecd63d0298b0fba3d586fcfb74ec9fdeb7f673fa`  
		Last Modified: Mon, 16 Oct 2023 18:47:08 GMT  
		Size: 2.3 MB (2342688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4afc6a2288f3616e27b1a3a04d90142c8670c80dc7156468262b95b58c0890f`  
		Last Modified: Mon, 16 Oct 2023 18:47:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66706788b67f9062b71f6f35d57f96cb85def5030722277f90d7102b7829dcb1`  
		Last Modified: Mon, 16 Oct 2023 19:27:18 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45738366bf6e97c1785529dc49baddfcabfb96f95c1fd25498973da41baa0769`  
		Last Modified: Mon, 16 Oct 2023 19:27:18 GMT  
		Size: 901.7 KB (901727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebed4246a56a80cb04d16e11fa0cea2f6330aac4f18545d75b3ac1fae5a66e25`  
		Last Modified: Mon, 16 Oct 2023 19:27:20 GMT  
		Size: 11.4 MB (11364034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0079e4ba77f8bcef7b95d45011f2eac18ddd60ce2134db6f289c699f9a2f7a`  
		Last Modified: Mon, 16 Oct 2023 19:27:35 GMT  
		Size: 115.5 MB (115522349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4db652e2ace0bccf6a3e8c23720e9c222a4194f366110b75d51f0cbf84b67a`  
		Last Modified: Mon, 16 Oct 2023 19:27:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:alpine`

```console
$ docker pull ghost@sha256:73f1619e47551cfdd81ae6e2d179951a7083b1e3f1d12055faa580ed0329ea6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:01bfb3bb2b469969a6abce07e6d28bd722576dbff07334e9deede599e6df0dcc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162046385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8905904f7279079eafd012f08974777c420f8cd0e56b1bf19498822357a281`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 16:24:20 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 16:24:29 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 16:24:30 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 16:24:34 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 16:24:34 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 16:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:24:35 GMT
CMD ["node"]
# Mon, 16 Oct 2023 16:54:20 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 16:54:21 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 16:54:21 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 16:54:21 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 16:54:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 16:54:44 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 16:56:23 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 16:56:25 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 16:56:25 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 16:56:25 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 16:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:56:26 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 16:56:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033f54f0a5153baf8a5e40f815c7bbd9c27ad232b9efcd9ff87ea37b52e34b45`  
		Last Modified: Mon, 16 Oct 2023 16:32:59 GMT  
		Size: 47.9 MB (47882552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd229524656b7cc4fcfbd5c8fdc4a289f6289ab2ff8f51aa1281dead0be417`  
		Last Modified: Mon, 16 Oct 2023 16:32:52 GMT  
		Size: 2.3 MB (2342744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7bbada826e20aeaca8697ad1260b2c445ef2fc64180fdb5d241fc0cc2088ab`  
		Last Modified: Mon, 16 Oct 2023 16:32:52 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cc9564647686a90e0c8abd5e279ce306318c321d05da54fff693504a19acaf`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 11.3 KB (11313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b4092a87622ce9a33c8ece18ce7b5427ad4de86d543bf2b99bdaa617f4684`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 857.7 KB (857732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcc6b768d949f8fe698871e18ff797a976210c28cd3a3f6d529b945c3fbb2e0`  
		Last Modified: Mon, 16 Oct 2023 16:57:30 GMT  
		Size: 11.4 MB (11363862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288f4022ec0c8d75572d56fb277ef32d2e5f945996f983da2ef177b3d811c07d`  
		Last Modified: Mon, 16 Oct 2023 16:57:45 GMT  
		Size: 96.2 MB (96208576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541a857a8bb4173584aa54ea0b22a84ab77f96dacea4ea34251a8f2367f3f553`  
		Last Modified: Mon, 16 Oct 2023 16:57:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:b1fca6a94245a7cbdb3582b9ce19fc1d9178a67324fc0089ce089f2409ee9656
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167834934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15aeaef2ca61598182ed319d7386c4f5f1d6b3a8cd5ae55b4492fd25c70c59c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 18:38:03 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:14:14 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 19:14:15 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:14:23 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 19:14:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:14:24 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:14:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 20:14:35 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 20:14:35 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:14:35 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:15:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:15:23 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:26:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:26:23 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:26:23 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:26:23 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 20:26:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:26:23 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:26:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f415473d39909779a9ced4eb567865bb60bd8c4bd0a63d8cc070885988fe9dd`  
		Last Modified: Mon, 16 Oct 2023 19:58:33 GMT  
		Size: 46.6 MB (46604107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97978632cc851576f0cb7237ebfdcdcf729523a53bd29648a9db888a404e74ff`  
		Last Modified: Mon, 16 Oct 2023 19:58:21 GMT  
		Size: 2.3 MB (2333251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88acc3a37de25984709560c7b1c378e78d0e0d88e4af4955f0603baefca2fb1b`  
		Last Modified: Mon, 16 Oct 2023 19:58:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cb37582abdc30ac7e6422025f85da3db251ed3d992fe772ad465d284ab04d2`  
		Last Modified: Mon, 16 Oct 2023 20:26:33 GMT  
		Size: 11.5 KB (11482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1352921cd650024ee4d2b7a78a2a3a29320681217ec5af19eac875ba8bd7b6`  
		Last Modified: Mon, 16 Oct 2023 20:26:34 GMT  
		Size: 852.1 KB (852055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56eb4e71d8f5944b338f71835ba3d5f49297f1ba4b7c052aa6a04d5dbd58be`  
		Last Modified: Mon, 16 Oct 2023 20:26:37 GMT  
		Size: 11.4 MB (11369871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6243bf3bed6d9f8cc3bd02cc5385c279a427db697c79e7e01bd93bb31344edb`  
		Last Modified: Mon, 16 Oct 2023 20:27:00 GMT  
		Size: 103.6 MB (103550722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d538e944dce2e79d055494a7a15d7e36dc705930108f10b774df3b2efbb29e`  
		Last Modified: Mon, 16 Oct 2023 20:26:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:30fd89f37f4a389c1db61286b087662ba8149d5ebda4af097749a1ec97532455
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166760006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6c2e10a4f99672014e34d71c961c992241186d0e004f894a053286795e71d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:29 GMT
ADD file:7f36c30ba2b714d09a8650dba1545abdf892443dadbe9113b9a166b84ba7ac3f in / 
# Mon, 07 Aug 2023 19:57:29 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 18:46:32 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:28:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 19:28:16 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:28:25 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 19:28:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:28:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:28:26 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:42:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 20:42:49 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 20:42:49 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:42:49 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:43:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:43:12 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:51:10 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:51:14 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:51:14 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:51:14 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 20:51:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:51:14 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:51:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b82e4fd40279a40aa2eecd301fabb2dca254727cc09daa8d0caf69ac28c44af1`  
		Last Modified: Mon, 07 Aug 2023 19:58:08 GMT  
		Size: 2.9 MB (2869425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3586eebdb95577161ff16425f85eb8feba2c58c486c9460b012d7ec660d60cb`  
		Last Modified: Mon, 16 Oct 2023 20:14:54 GMT  
		Size: 46.1 MB (46120148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90067fee2ddb35cd44b2d22dbbbcc478ef2fce71bd4eb56b7b2cc998b6d05f79`  
		Last Modified: Mon, 16 Oct 2023 20:14:46 GMT  
		Size: 2.3 MB (2333227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbf104935b929e86d3a4aa6960b128643eb9abd9f5ca8cc98d3d43e32efd408`  
		Last Modified: Mon, 16 Oct 2023 20:14:45 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4f0fbc19f92f3a73ac44c207e4d0d358ad2e1d25b88617a09926b44c6bc3a9`  
		Last Modified: Mon, 16 Oct 2023 20:52:27 GMT  
		Size: 11.3 KB (11281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c377b31bf856bdd5320715b41552621eed54cc17b3e713cac5e558c919a449d`  
		Last Modified: Mon, 16 Oct 2023 20:52:27 GMT  
		Size: 781.9 KB (781860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1049d5f1e4eefb9d7138a0264b55d681e076e962183abca5245996cd0c97a231`  
		Last Modified: Mon, 16 Oct 2023 20:52:31 GMT  
		Size: 11.4 MB (11364177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dd375f004183a4d4524b7474a0d0f69d02841fb9fa76627092bfb99d78d405`  
		Last Modified: Mon, 16 Oct 2023 20:52:52 GMT  
		Size: 103.3 MB (103278894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341163b15ef28dd94a2af354bcf7a344c1b72d618837b73cc52f93d54cf08b95`  
		Last Modified: Mon, 16 Oct 2023 20:52:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:e7ff98a9f5e015ead631388c78eeab289d840ac7db81aaceaa8c40c90f8f6042
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181013595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1705e5c5897236c3cbd412643f6b898737292091d2127fddec9ccf4ffb3d17a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Oct 2023 17:56:18 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 18:17:51 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64)           ARCH='x64'           CHECKSUM="b02028add9898575516a2626a5f1a262f080291d8f253ba1fd61cedb0e476591"           ;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && apk del .build-deps   && node --version   && npm --version
# Mon, 16 Oct 2023 18:17:52 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 18:17:56 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 16 Oct 2023 18:17:56 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 18:17:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:17:56 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:18:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 16 Oct 2023 19:18:50 GMT
RUN apk add --no-cache 		bash
# Mon, 16 Oct 2023 19:18:50 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:18:50 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:19:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:19:12 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:26:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='su-exec node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='su-exec node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		su-exec node yarn cache clean; 	su-exec node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:26:07 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:26:07 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:26:07 GMT
COPY file:87209c4c75826f5d839c2f3270a782740f42eecf4bc96b2f6dbae79b08c17e21 in /usr/local/bin 
# Mon, 16 Oct 2023 19:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:26:08 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:26:08 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9eeebfedfff83c826fdc684aad595811a2e46c4a1b4fbf9c7d9b9d8413b6a5`  
		Last Modified: Mon, 16 Oct 2023 18:47:14 GMT  
		Size: 47.6 MB (47611982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf6c5ea44d1eedc0d68e6beecd63d0298b0fba3d586fcfb74ec9fdeb7f673fa`  
		Last Modified: Mon, 16 Oct 2023 18:47:08 GMT  
		Size: 2.3 MB (2342688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4afc6a2288f3616e27b1a3a04d90142c8670c80dc7156468262b95b58c0890f`  
		Last Modified: Mon, 16 Oct 2023 18:47:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66706788b67f9062b71f6f35d57f96cb85def5030722277f90d7102b7829dcb1`  
		Last Modified: Mon, 16 Oct 2023 19:27:18 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45738366bf6e97c1785529dc49baddfcabfb96f95c1fd25498973da41baa0769`  
		Last Modified: Mon, 16 Oct 2023 19:27:18 GMT  
		Size: 901.7 KB (901727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebed4246a56a80cb04d16e11fa0cea2f6330aac4f18545d75b3ac1fae5a66e25`  
		Last Modified: Mon, 16 Oct 2023 19:27:20 GMT  
		Size: 11.4 MB (11364034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0079e4ba77f8bcef7b95d45011f2eac18ddd60ce2134db6f289c699f9a2f7a`  
		Last Modified: Mon, 16 Oct 2023 19:27:35 GMT  
		Size: 115.5 MB (115522349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4db652e2ace0bccf6a3e8c23720e9c222a4194f366110b75d51f0cbf84b67a`  
		Last Modified: Mon, 16 Oct 2023 19:27:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:latest`

```console
$ docker pull ghost@sha256:5592f7cc64c2736cbc11e7b5ba8c4a260cfa3717f5a5e511cf2a2d57bad7f6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ghost:latest` - linux; amd64

```console
$ docker pull ghost@sha256:937d78eb0a678aba143a95fd994df37034b13e1815d95bd3bb176cd7c4466b1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191983695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36740855a01dac184ea9b64bbe21d91bd84bee13cda8ce75ee58a923975b8534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:08:07 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 16:26:32 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 16:26:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 16:26:57 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 16:27:09 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 16:27:09 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 16:27:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:27:10 GMT
CMD ["node"]
# Mon, 16 Oct 2023 16:51:55 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 16:52:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 16:52:06 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 16:52:06 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 16:52:27 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 16:52:28 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 16:54:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 16:54:03 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 16:54:03 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 16:54:03 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 16:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 16:54:03 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 16:54:03 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e37ba7d55cf627d7a515836792f8cbcae450b50ddacf7479423e96b99d75656`  
		Last Modified: Thu, 12 Oct 2023 00:15:23 GMT  
		Size: 4.2 KB (4187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002620df87aa0387e2265b1a0a8a4cf6bc3f390a34ddbef1651cd202ead062f8`  
		Last Modified: Mon, 16 Oct 2023 16:35:30 GMT  
		Size: 46.4 MB (46426623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30f6d630a337c355d08f613f7d6e86c38b8c3e4e8f24784aa4e99d597aa781b`  
		Last Modified: Mon, 16 Oct 2023 16:35:23 GMT  
		Size: 2.8 MB (2770727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72e258397901700c61a75bf99c66b41d306e5fd9080a6ac0c710026e94abf27`  
		Last Modified: Mon, 16 Oct 2023 16:35:23 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a330a83dc7a84b2f7f0bafef6e708e1b74e0ae74d419081f713dcd4154a17`  
		Last Modified: Mon, 16 Oct 2023 16:56:53 GMT  
		Size: 1.5 MB (1469905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9077330d689580cc1928b6364c9666be42038efde1e5504eb0d285823a93402c`  
		Last Modified: Mon, 16 Oct 2023 16:56:56 GMT  
		Size: 11.4 MB (11363818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068bf5111bf90fa03eda13cb2486cf61396d2e277ae00060a2c7ff066192028c`  
		Last Modified: Mon, 16 Oct 2023 16:57:11 GMT  
		Size: 98.5 MB (98529575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40081701b49d3a882ea186b0e95b148993d28342e63d86dff1e336c12ca9053`  
		Last Modified: Mon, 16 Oct 2023 16:56:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6adf4643e2ea2fca923d845bcb53fd858b7a972703ddaadfdda60e6a64bec30c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205206730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea49cc33999704af6f3a575329a775783d415b1b8178d6a936eaf10255c9e199`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:29 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Wed, 11 Oct 2023 17:42:29 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 23:19:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 20:07:47 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 20:08:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 20:08:23 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 20:08:36 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 20:08:36 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 20:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:08:36 GMT
CMD ["node"]
# Mon, 16 Oct 2023 20:34:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 20:34:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 20:34:52 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 20:34:52 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 20:35:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 20:35:15 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 20:42:29 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 20:42:33 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 20:42:33 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 20:42:33 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 20:42:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 20:42:34 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 20:42:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c88fd62ab16546a4c895d6ad8f01a3dfe22d1a07fe074491f45ef80da25431`  
		Last Modified: Thu, 12 Oct 2023 00:24:46 GMT  
		Size: 4.2 KB (4171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a06f6ae103ebd030decce00a4cc8e32a19ef0f8ad0276914f835369507a723`  
		Last Modified: Mon, 16 Oct 2023 20:17:31 GMT  
		Size: 43.0 MB (43022548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8d5077827a14ee0d8965c56b27f5afe4981eb37430981b13aea6302839c84e`  
		Last Modified: Mon, 16 Oct 2023 20:17:23 GMT  
		Size: 2.8 MB (2760725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef44d15f789fb7c5f486026196e533df5be09b7ae5c775eba6f1ff24d7e8089d`  
		Last Modified: Mon, 16 Oct 2023 20:17:23 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e2b0913a8496be4fd9c970344fd197899227dbd2cb30a3790f96009d5f8624`  
		Last Modified: Mon, 16 Oct 2023 20:51:33 GMT  
		Size: 1.4 MB (1438454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba40f16ee45cf5955ea3604046098cbd15e5b6587f6f44ae10540cee6bb6e64`  
		Last Modified: Mon, 16 Oct 2023 20:51:40 GMT  
		Size: 11.4 MB (11364177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92412f18d48fff0e8a9c63a5058848a398133924ddb3e592d96b7a18d75d4e39`  
		Last Modified: Mon, 16 Oct 2023 20:52:12 GMT  
		Size: 120.0 MB (120036650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae8f99c87ebe0414c89160d74606acc5004a85f3b29cf1613a8e74467f62a2`  
		Last Modified: Mon, 16 Oct 2023 20:51:32 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:d061370a7ed9577fa730a31b63af29de3af0929065d45fefe4ae2cf42f639bd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209234892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fdd52a2c90a1f101ecf18520b41cc2bf6b80322788a54d59eb648b4015af87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:40:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 18:40:47 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 18:41:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 18:41:10 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 18:41:20 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 18:41:21 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 18:41:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:41:21 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:11:55 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 19:12:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 19:12:06 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:12:06 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:12:28 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:12:29 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:18:40 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:18:46 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:18:46 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:18:46 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 19:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:18:46 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:18:46 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c0b58a4c2a0d10e68fc166330a6deedc851b3ac46fef98c8bbb7d9d4fc032c`  
		Last Modified: Thu, 12 Oct 2023 03:32:17 GMT  
		Size: 4.2 KB (4191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5bcae6c0230e5d06b9117aa2798d47e893dd47443e5217f7f8b182dfabd4a8`  
		Last Modified: Mon, 16 Oct 2023 18:49:35 GMT  
		Size: 46.5 MB (46516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d075541aab707d326dbaa35c19794a83ce389d115fbe5474101dd10af237e4b`  
		Last Modified: Mon, 16 Oct 2023 18:49:29 GMT  
		Size: 2.8 MB (2770668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1204d42b94792c6a46927ba64709a7e29dfd0bcdf0d44149fcb8d4f36fb0ca4`  
		Last Modified: Mon, 16 Oct 2023 18:49:29 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1c31c66d5c8e1c2fde8957ebc0bf09ce40bb8a086a5bed66ea2ced65693657`  
		Last Modified: Mon, 16 Oct 2023 19:26:19 GMT  
		Size: 1.4 MB (1402415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3600194007499e5a20997f869734637469035b34683de5c4749cf06f085c9ea`  
		Last Modified: Mon, 16 Oct 2023 19:26:22 GMT  
		Size: 11.4 MB (11363908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34aee59abe6842d523da00dadbed2a288ff9e6d418871275eeb109ef837f482`  
		Last Modified: Mon, 16 Oct 2023 19:26:59 GMT  
		Size: 117.1 MB (117112037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc23cf7641ab01d4964d24bd31e5252407ec65b41a7c5743cacf207e2ef28d`  
		Last Modified: Mon, 16 Oct 2023 19:26:19 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:4e69aba2bf77b98baf77e320ac58ba755bb8b0bbb307069642502dcfeac7ccbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205916586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fad4b5ee20e2fbb3f25e531acc6783725a217a57ccb9a846369d558041c192`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:53 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Wed, 11 Oct 2023 17:44:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 21:20:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 17:41:00 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 17:42:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 17:42:13 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 17:42:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 17:42:54 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 17:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 17:42:55 GMT
CMD ["node"]
# Mon, 16 Oct 2023 18:05:44 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 18:06:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 18:06:18 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 18:06:18 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 18:06:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 18:06:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 18:06:51 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 18:06:51 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 18:20:02 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 18:20:17 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 18:20:17 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 18:20:19 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 18:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 18:20:28 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 18:20:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea410cd4a5e719800e963888d39e95c3304f03c9b6274ca138e124cca600b1`  
		Last Modified: Wed, 11 Oct 2023 22:19:07 GMT  
		Size: 4.2 KB (4185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc596c427dd68b1259ccfe96dd02ae17e7c2322e199ae7ab0e11be036711d4a9`  
		Last Modified: Mon, 16 Oct 2023 17:50:15 GMT  
		Size: 48.5 MB (48548480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56751402a723c92fc764a54ad4a35bea6dc20b3f1aef689a134948a34829c50`  
		Last Modified: Mon, 16 Oct 2023 17:50:06 GMT  
		Size: 2.8 MB (2770826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809fd57bad8306838adc75d8c5fd3a928c6e777d7cfbc05b554384f3b6d07a7`  
		Last Modified: Mon, 16 Oct 2023 17:50:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c882a4939693aa1cedc553358ab0380431ee1f3fb957d22adfa47848f4a9094`  
		Last Modified: Mon, 16 Oct 2023 18:20:48 GMT  
		Size: 1.4 MB (1392744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90e1477a0d32c2f11bf1de5b8512520b19e9dfb1292762384cff02c32fef54`  
		Last Modified: Mon, 16 Oct 2023 18:20:51 GMT  
		Size: 11.4 MB (11365705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a586bf88d0b231f22a5e5121f3b7414a9195eb5f7b2e8eef3125c864abdf8a`  
		Last Modified: Mon, 16 Oct 2023 18:21:15 GMT  
		Size: 106.5 MB (106539929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897acd0eb7b9fe55672d658b56813bfd024312ffd0e0ebca4d16d5a60172ed7`  
		Last Modified: Mon, 16 Oct 2023 18:20:47 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:4000abe65c29881fb22442927bbbc18a9154762533c7fa8b6f8157875b3ba941
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198196985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ac4509b83f162b3a20d8e141d5a3c0fa438eaab2704243efa6b50881922595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:11:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Mon, 16 Oct 2023 19:26:33 GMT
ENV NODE_VERSION=18.18.2
# Mon, 16 Oct 2023 19:26:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version
# Mon, 16 Oct 2023 19:27:00 GMT
ENV YARN_VERSION=1.22.19
# Mon, 16 Oct 2023 19:27:11 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version
# Mon, 16 Oct 2023 19:27:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 16 Oct 2023 19:27:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:27:11 GMT
CMD ["node"]
# Mon, 16 Oct 2023 19:48:20 GMT
ENV GOSU_VERSION=1.16
# Mon, 16 Oct 2023 19:48:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 16 Oct 2023 19:48:29 GMT
ENV NODE_ENV=production
# Mon, 16 Oct 2023 19:48:29 GMT
ENV GHOST_CLI_VERSION=1.25.3
# Mon, 16 Oct 2023 19:49:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force
# Mon, 16 Oct 2023 19:49:18 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 16 Oct 2023 19:49:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 16 Oct 2023 19:49:19 GMT
ENV GHOST_VERSION=5.69.0
# Mon, 16 Oct 2023 19:55:30 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*
# Mon, 16 Oct 2023 19:55:46 GMT
WORKDIR /var/lib/ghost
# Mon, 16 Oct 2023 19:55:46 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 16 Oct 2023 19:55:46 GMT
COPY file:303989b132b5193e832753e2c7236a4050fdc0fe60a54dc1f0c4a44422a2d1ca in /usr/local/bin 
# Mon, 16 Oct 2023 19:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2023 19:55:47 GMT
EXPOSE 2368
# Mon, 16 Oct 2023 19:55:47 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1232a8d204040b3d9f8ce99e019405b6bc475472eb81c144dfad2dbe15237f97`  
		Last Modified: Thu, 12 Oct 2023 04:28:13 GMT  
		Size: 4.2 KB (4186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed9e3be403a99840a356edb58b5817add20d87956629a24d8037a390b69891`  
		Last Modified: Mon, 16 Oct 2023 19:32:23 GMT  
		Size: 46.3 MB (46288457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3467ff7578bfab1ad4a9107dc35d1663bbdd0ac3c5ec66ce2aa21b3364e00d1`  
		Last Modified: Mon, 16 Oct 2023 19:32:15 GMT  
		Size: 2.8 MB (2771451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80606ed396e3b219a063868a03be8770c9f3ace0f5528c693eeeb422d8d9fc87`  
		Last Modified: Mon, 16 Oct 2023 19:32:15 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ad27a74dde3d5b45e18468ec98608732d2340fe547593713f074aafd22a8`  
		Last Modified: Mon, 16 Oct 2023 19:56:12 GMT  
		Size: 1.4 MB (1436034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4f903be8fbd39002d2fa421bbb5eeed433cc6358f08058741efd790e61eee3`  
		Last Modified: Mon, 16 Oct 2023 19:56:15 GMT  
		Size: 11.4 MB (11363693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bb59920a1f8634233d4b6370eb8dc3269c70f154b91fb8208588afef2f4cad`  
		Last Modified: Mon, 16 Oct 2023 19:56:32 GMT  
		Size: 106.7 MB (106675249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d81c3e8f50e4af366c889fd3d92aea6f358ac6987974de680010c6cca710c58`  
		Last Modified: Mon, 16 Oct 2023 19:56:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
