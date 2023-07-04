## `swift:jammy-slim`

```console
$ docker pull swift@sha256:65bb74437c4693738015666f14ea7d393cefcbff98c9fec83c0afd3cf807f5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:11d933000942649e7cba969fe04c954feaab502aa96c7c714c6b5510665d5dd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132602343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f9f79bd2dc0e0b6fecd369945d43dada626fa590bdb29137465f57975da473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:51:44 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 16 Jun 2023 00:51:44 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 16 Jun 2023 00:54:44 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:54:44 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 16 Jun 2023 00:54:45 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 16 Jun 2023 00:54:45 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Fri, 16 Jun 2023 00:54:45 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Fri, 16 Jun 2023 00:54:45 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 16 Jun 2023 00:54:45 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 16 Jun 2023 00:55:14 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef4ae49bc9ef6ae1fdfbe336215669c3f23886481cbfe3c90f332db82b949d6`  
		Last Modified: Fri, 16 Jun 2023 01:19:50 GMT  
		Size: 19.2 MB (19190587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752e9006799106a5f81866bd44c7128762d40bc4c8230e5c648fac1fa0bcfa2e`  
		Last Modified: Fri, 16 Jun 2023 01:19:59 GMT  
		Size: 83.0 MB (82980717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:16bde1f8593980c684b07b7326e093ccf5d59b8116219f0547ba36f15c84dcf5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129256395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb2f1ac1b9b8d62e389c2f1e36a4fa8fe0d2d82170abfe6d1d817758685d0c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:11:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Jul 2023 15:11:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Jul 2023 15:13:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:13:41 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 04 Jul 2023 15:13:41 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 04 Jul 2023 15:13:41 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Tue, 04 Jul 2023 15:13:41 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Tue, 04 Jul 2023 15:13:41 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Jul 2023 15:13:41 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Jul 2023 15:14:23 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3283785431ae84ccfcc8046c9f014c9ab3b49ddec04aa7aef6a7a9ce4860deb`  
		Last Modified: Tue, 04 Jul 2023 15:25:56 GMT  
		Size: 19.1 MB (19087587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6323f1becc8509dd06b535a4f51dd34e5b05b5d9016136758686b0d16f3e1c50`  
		Last Modified: Tue, 04 Jul 2023 15:26:01 GMT  
		Size: 81.8 MB (81777797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
