## `swift:focal-slim`

```console
$ docker pull swift@sha256:107ae5100281b3640469137782dcce668e6f2190311a2891f7579ed40aaac171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:c8b3ffe31d89c65875b1cdce4ac941bc5ca273dfff3c6f9cdb3a03d84b2320fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135121570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559a498f0a6da6c7829dfaccc41f703110021053ee1e9b91b8328b9dcb15d573`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 00:15:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 04 Mar 2022 00:15:33 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 04 Mar 2022 00:15:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 04 Mar 2022 00:15:46 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 04 Mar 2022 00:15:46 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 16 Mar 2022 19:05:04 GMT
ARG SWIFT_BRANCH=swift-5.6-release
# Wed, 16 Mar 2022 19:05:04 GMT
ARG SWIFT_VERSION=swift-5.6-RELEASE
# Wed, 16 Mar 2022 19:05:04 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 16 Mar 2022 19:05:04 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.6-release SWIFT_VERSION=swift-5.6-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 16 Mar 2022 19:06:34 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36393c7dc5a7a0e032b3ed3acc29e52ee120ebf18bf88fa5547731aab2ea7ba6`  
		Last Modified: Fri, 04 Mar 2022 00:51:03 GMT  
		Size: 22.3 MB (22251127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa1731a40c3583ec316bca48f61b9b3fc68860d36c5459ce57ddee9ad71bdac`  
		Last Modified: Wed, 16 Mar 2022 19:28:23 GMT  
		Size: 84.3 MB (84304692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:focal-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:a4a776def3f25b141ac0f636a33924abe3f67f2d232e7176fe497256ad50b303
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129464452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25f87be49e75f065e40aa10c2d98537c19853e0984e070b7a6def45e5403f84`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 14:51:43 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 19 Mar 2022 14:51:44 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 19 Mar 2022 14:51:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:51:58 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 19 Mar 2022 14:51:59 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Sat, 19 Mar 2022 14:52:00 GMT
ARG SWIFT_BRANCH=swift-5.6-release
# Sat, 19 Mar 2022 14:52:01 GMT
ARG SWIFT_VERSION=swift-5.6-RELEASE
# Sat, 19 Mar 2022 14:52:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 19 Mar 2022 14:52:03 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.6-release SWIFT_VERSION=swift-5.6-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 19 Mar 2022 14:53:24 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f441fad5ffa9e4b5e904a67631216f60925b540a0391167608a2247165daf7b`  
		Last Modified: Sat, 19 Mar 2022 14:59:45 GMT  
		Size: 22.0 MB (22032349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e166ad2e6e24a16c8ebf15a59257e278a04e16dd38b787cc9b8d727d65db377`  
		Last Modified: Sat, 19 Mar 2022 14:59:54 GMT  
		Size: 80.3 MB (80262486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
