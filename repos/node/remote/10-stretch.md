## `node:10-stretch`

```console
$ docker pull node@sha256:1e8c3b26a17b53b4faabccd886d262ed3c58ceb07b08795783c53ec9403432fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `node:10-stretch` - linux; amd64

```console
$ docker pull node@sha256:3817b91ad67604a053ee2a765226ab55c6de9064f3cdf4904f73d8bd6c54c92a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349049741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7f33f1e657d4a293ac709cd5c8db1e2bb25f2c99bb71d76d163b4cfe9806`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:08:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:10:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:01:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 31 Mar 2021 05:08:56 GMT
ENV NODE_VERSION=10.24.0
# Wed, 31 Mar 2021 05:09:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     74F12602B6F1C4E913FAA37AD3A89613643B6201     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     A48C2BEE680E841632CD4E44F07496B3EB3C1762     108F52B48DB57BB0CC439B2997B01419BD92F80A     B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 31 Mar 2021 05:09:04 GMT
ENV YARN_VERSION=1.22.5
# Wed, 31 Mar 2021 05:09:08 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 31 Mar 2021 05:09:09 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 31 Mar 2021 05:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 05:09:09 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae835e2c68ef1d48a4ffef72547a79926019aec6a2bbeb5372f1e832ef453dd`  
		Last Modified: Tue, 30 Mar 2021 23:17:49 GMT  
		Size: 49.8 MB (49787075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5254dc317968c943c4321cdbf0364a6a47c833296b3f45e3bd27aa4efe28c865`  
		Last Modified: Tue, 30 Mar 2021 23:18:46 GMT  
		Size: 214.3 MB (214347447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f76fdfa8e8784238b141aaa54fa1862aef5348665431168a675b1f730abfa8`  
		Last Modified: Wed, 31 Mar 2021 05:15:35 GMT  
		Size: 4.2 KB (4191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86ba39ada9c0ed0b29f2fd6fa536f662695d8f9ac153dd6b7f59a16059a3a40`  
		Last Modified: Wed, 31 Mar 2021 05:22:55 GMT  
		Size: 21.4 MB (21417563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff90ed33a31e254e67fd73dcd0a85ebc56cbba33a1b525cfca208b9d40475c`  
		Last Modified: Wed, 31 Mar 2021 05:22:50 GMT  
		Size: 2.5 MB (2484099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200b4a15ad5b30963f56abc772c3399b5694007052469661b5318224b8aaf778`  
		Last Modified: Wed, 31 Mar 2021 05:22:50 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:10-stretch` - linux; arm variant v7

```console
$ docker pull node@sha256:345e2612402ee63a69f7b79cfb7ad9b2d363cc12eae6f8da57229417fd0dc31b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.8 MB (319788188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbdab31416b16e2a44a9afb1d0de46e9c729ffa5492b9021052972b80c0f862`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 30 Mar 2021 23:11:31 GMT
ADD file:65b5cf73b0b90f1f459a64d5706f2420deed7cdc5a9e13abacf5bcb05cc3138d in / 
# Tue, 30 Mar 2021 23:11:34 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:29:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 01:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:32:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 02:50:55 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 31 Mar 2021 03:05:12 GMT
ENV NODE_VERSION=10.24.0
# Wed, 31 Mar 2021 03:05:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     74F12602B6F1C4E913FAA37AD3A89613643B6201     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     A48C2BEE680E841632CD4E44F07496B3EB3C1762     108F52B48DB57BB0CC439B2997B01419BD92F80A     B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 31 Mar 2021 03:05:26 GMT
ENV YARN_VERSION=1.22.5
# Wed, 31 Mar 2021 03:05:32 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 31 Mar 2021 03:05:33 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 31 Mar 2021 03:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 03:05:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:80ad3ae4821828f32ce9b3e0f76c3c8f157a7f111e64ffad3ba40287904dfc63`  
		Last Modified: Tue, 30 Mar 2021 23:18:47 GMT  
		Size: 42.1 MB (42120250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b448d9cdc0300784b14c4a254300d86c316aca568d8b068cdc585ff456ccca`  
		Last Modified: Wed, 31 Mar 2021 01:39:43 GMT  
		Size: 9.9 MB (9939722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845e857248fe8de10609204e4eb4db8efcbb33c6a2f9e10b7d3efe4c3c625be`  
		Last Modified: Wed, 31 Mar 2021 01:39:41 GMT  
		Size: 3.9 MB (3921214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2026eb34d858c1a9d59647eb6a6d3c28cd258eaa588cf3b99b35ac0d590fab2a`  
		Last Modified: Wed, 31 Mar 2021 01:40:05 GMT  
		Size: 46.1 MB (46127566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ee28f5fa017782798168c4413003d88659984a23db27ea45095dcd3b95114`  
		Last Modified: Wed, 31 Mar 2021 01:41:08 GMT  
		Size: 195.0 MB (195008044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c8f00870b79f11de48b5e3f52070304566894d2760443093edb68ddd029e89`  
		Last Modified: Wed, 31 Mar 2021 03:10:45 GMT  
		Size: 4.2 KB (4178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab2a42ef0da4c6d1096f5891a50de2e76c8b1b8cfac6aa8e8190b648553d21e`  
		Last Modified: Wed, 31 Mar 2021 03:16:41 GMT  
		Size: 20.2 MB (20223114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efca8368414fb3072dbdb9f8506a0d4dd9e12671d98d91e55c4e551c163c890`  
		Last Modified: Wed, 31 Mar 2021 03:16:31 GMT  
		Size: 2.4 MB (2443807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56c5e29114d7c8d9bafd83c1939216e8db8a833b5f5d542c8b419f58a264ec2`  
		Last Modified: Wed, 31 Mar 2021 03:16:33 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:10-stretch` - linux; arm64 variant v8

```console
$ docker pull node@sha256:bda11e320e164d637d7dd45474ee859ac5e938bac6461e12b370d7a60c1b1498
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330921310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4533f3c37c22c95c1a28347668e7338f563d3506ae702e2e47df06b666731d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:45 GMT
ADD file:0546f28e5d1be54699d1e0756275203da731735b3212f2ff1a87cd7f8dcc9049 in / 
# Tue, 30 Mar 2021 21:49:50 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:22:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 00:23:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:25:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:03:52 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 31 Mar 2021 01:17:02 GMT
ENV NODE_VERSION=10.24.0
# Wed, 31 Mar 2021 01:17:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     74F12602B6F1C4E913FAA37AD3A89613643B6201     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     A48C2BEE680E841632CD4E44F07496B3EB3C1762     108F52B48DB57BB0CC439B2997B01419BD92F80A     B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 31 Mar 2021 01:17:17 GMT
ENV YARN_VERSION=1.22.5
# Wed, 31 Mar 2021 01:17:24 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 31 Mar 2021 01:17:25 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 31 Mar 2021 01:17:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 01:17:27 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:9317dc7ea567b49ade0ea730b5530d1363b065549e8b75a198e0b60bdde1f1d7`  
		Last Modified: Tue, 30 Mar 2021 21:56:46 GMT  
		Size: 43.2 MB (43177588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf1b7b1bdfdc23af33da7d1fc9670524e63a8408bb04de9aebdf95979c5635`  
		Last Modified: Wed, 31 Mar 2021 00:33:12 GMT  
		Size: 10.2 MB (10201033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4446041554682b465ef9a0e853a5067e7d794fa1c840946d140beab2ddeb51`  
		Last Modified: Wed, 31 Mar 2021 00:33:09 GMT  
		Size: 4.1 MB (4096741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0b477e68dd7171c7df2dfc66cd994be553e0679dd5c2083048d10d5a29363a`  
		Last Modified: Wed, 31 Mar 2021 00:33:40 GMT  
		Size: 47.7 MB (47735121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8e162dfd38e34eeb2178da6fcb11b12f16ffa8bd96bbd6f0207dd5eceb7732`  
		Last Modified: Wed, 31 Mar 2021 00:34:37 GMT  
		Size: 201.7 MB (201719845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4555bb0069db3ba305b69b0c2dc5b4f7a6f975683ef549b77c8e507a3e86a5a`  
		Last Modified: Wed, 31 Mar 2021 01:22:46 GMT  
		Size: 4.2 KB (4201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d67f108caad06c4987ec5782fd3388f1119369d169a7a05ab654b36867926fe`  
		Last Modified: Wed, 31 Mar 2021 01:28:41 GMT  
		Size: 21.5 MB (21502453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534bd4b6deb0609371ac6dd5f7f723836287606815eaddbb9cd363f2e98485d3`  
		Last Modified: Wed, 31 Mar 2021 01:28:35 GMT  
		Size: 2.5 MB (2484036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59786760238631bde166ba39f907298adc98116dbce8c5223c1ed0d9c72c1`  
		Last Modified: Wed, 31 Mar 2021 01:28:35 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
