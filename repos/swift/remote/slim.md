## `swift:slim`

```console
$ docker pull swift@sha256:c156ec5aeff52970e5ae86db71c3e4f05ce93957eb5e19b8fecff9a0a1049065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:26bccaf9ba8faa926e2ca94ce9b87aabfcff277557fb165a99e3cc57f5c387fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138987307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3cbe695a1430be40c0dd7caad9ae78ca3b70a5eedbf0626657b0464834559`
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
# Fri, 09 Dec 2022 02:53:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:53:39 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 09 Dec 2022 02:53:39 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 09 Dec 2022 02:53:39 GMT
ARG SWIFT_BRANCH=swift-5.7.1-release
# Fri, 09 Dec 2022 02:53:39 GMT
ARG SWIFT_VERSION=swift-5.7.1-RELEASE
# Fri, 09 Dec 2022 02:53:39 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 09 Dec 2022 02:53:39 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7.1-release SWIFT_VERSION=swift-5.7.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 09 Dec 2022 02:54:16 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da4fec8b39bc226e35ff11b6df2c1e7f3d7b5497c14bd49d28bfc635026ecfb`  
		Last Modified: Fri, 09 Dec 2022 03:29:26 GMT  
		Size: 19.1 MB (19111932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a041e0690e2a9feb6c4c992b15a74e7acd8226c53ccbf262e965b6453614c3`  
		Last Modified: Fri, 09 Dec 2022 03:29:36 GMT  
		Size: 89.4 MB (89446667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:4b62a2f65fe1377ea99beee42eb3a543ad180e74d87534d63d67aebf20097757
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135658427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4312f3279dd6eb3f2a32af12e4fafe80121e26ad0b640e7f01a9cfdd3bdaf61d`
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
# Fri, 09 Dec 2022 02:19:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:19:24 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 09 Dec 2022 02:19:24 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 09 Dec 2022 02:19:24 GMT
ARG SWIFT_BRANCH=swift-5.7.1-release
# Fri, 09 Dec 2022 02:19:24 GMT
ARG SWIFT_VERSION=swift-5.7.1-RELEASE
# Fri, 09 Dec 2022 02:19:24 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 09 Dec 2022 02:19:24 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7.1-release SWIFT_VERSION=swift-5.7.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 09 Dec 2022 02:20:00 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:10175de2f0c4f7d306f660ee073bce12b824c8012dd19b3c140aae053fabd1cc`  
		Last Modified: Thu, 08 Dec 2022 18:50:01 GMT  
		Size: 28.4 MB (28384475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c281e7fba87591a6d615bbd45d84cc901be1febefb8c6d191d04c3f3c9d89551`  
		Last Modified: Fri, 09 Dec 2022 02:26:53 GMT  
		Size: 19.0 MB (18997075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0970c1caa49e23a94cdf8ee2cd6f14808ab0d4789bd4f131e86563877206afe0`  
		Last Modified: Fri, 09 Dec 2022 02:27:01 GMT  
		Size: 88.3 MB (88276877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
