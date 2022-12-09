## `swift:latest`

```console
$ docker pull swift@sha256:3e34729977b092cd9a88076689103ac21e8436ad73c65c8f04008d97a6e03fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:3d9ebbff3b2033f7c1a2be9a7ae3fbe413a68761afb65cd5ceae857941933b13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.7 MB (685745401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a278339582efedb0c3abae86978b4fa3e901fc503af1b2f8c9cd8ec7af5e50b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:51:08 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 09 Dec 2022 02:51:09 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 09 Dec 2022 02:52:29 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:52:30 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 09 Dec 2022 02:52:30 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 09 Dec 2022 02:52:30 GMT
ARG SWIFT_BRANCH=swift-5.7.1-release
# Fri, 09 Dec 2022 02:52:30 GMT
ARG SWIFT_VERSION=swift-5.7.1-RELEASE
# Fri, 09 Dec 2022 02:52:30 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 09 Dec 2022 02:52:30 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7.1-release SWIFT_VERSION=swift-5.7.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 09 Dec 2022 02:53:13 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 09 Dec 2022 02:53:19 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a89c39ae29f9b99db84d92734425a9a32030ef3065b71fa83b745433f94f3e`  
		Last Modified: Fri, 09 Dec 2022 03:28:05 GMT  
		Size: 103.5 MB (103467095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c82c40c2c103dc7b60da9057cde656c7d22993ef6a3c4c7afc93616ee7fb37`  
		Last Modified: Fri, 09 Dec 2022 03:29:05 GMT  
		Size: 551.8 MB (551849373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1316360271d34b14d21ab874c2a0ff6262d9e62346f6d4476219717e7f49e5`  
		Last Modified: Fri, 09 Dec 2022 03:27:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:600746b43dafcdb291c66628f6eb9c9cb63d7fed12169459612c54a98cc80ec8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.4 MB (671359662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1841d8db44fe09131ea8b18e714523250d2400023dd56e29703b47a67cd13397`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:57 GMT
ADD file:429a55a11d4bcd15647d1316d9debd9ead4b4ab5c0b9146894d07c39aa814290 in / 
# Fri, 09 Dec 2022 01:46:57 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:16:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 09 Dec 2022 02:16:10 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 09 Dec 2022 02:17:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:17:57 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 09 Dec 2022 02:17:57 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 09 Dec 2022 02:17:57 GMT
ARG SWIFT_BRANCH=swift-5.7.1-release
# Fri, 09 Dec 2022 02:17:58 GMT
ARG SWIFT_VERSION=swift-5.7.1-RELEASE
# Fri, 09 Dec 2022 02:17:58 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 09 Dec 2022 02:17:58 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7.1-release SWIFT_VERSION=swift-5.7.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 09 Dec 2022 02:19:02 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 09 Dec 2022 02:19:13 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:10175de2f0c4f7d306f660ee073bce12b824c8012dd19b3c140aae053fabd1cc`  
		Last Modified: Thu, 08 Dec 2022 18:50:01 GMT  
		Size: 28.4 MB (28384475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312c6f3f5d8514bf1c60cdded89dca6ac3a0cf0e1be225dadadecb5bcbd5d990`  
		Last Modified: Fri, 09 Dec 2022 02:25:41 GMT  
		Size: 100.7 MB (100669729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b31565a46a1097f10e7a27bc309bc7c908cdde5cc398ca9fbab42287e611f`  
		Last Modified: Fri, 09 Dec 2022 02:26:33 GMT  
		Size: 542.3 MB (542305232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5deaf5fc0d6ada872700d7813a1870cd4fcec269253f5e615926be6c3f50cc`  
		Last Modified: Fri, 09 Dec 2022 02:25:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
