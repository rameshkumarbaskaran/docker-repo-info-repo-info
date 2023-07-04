## `swift:focal-slim`

```console
$ docker pull swift@sha256:8fcaf486a73feeba0dd8061cd6961a200177120e474d2067afab4a25d127f84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:6782ef0819f8e6a9dfffc11cbe30f3bd90e5a1180f9595a38ff40ed79d784f6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133768399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db64186618d111edd9a380dd41b7354f4a16587952062e9d6a359b728f919ffc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:55:23 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 16 Jun 2023 00:55:23 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 16 Jun 2023 00:55:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:55:58 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 16 Jun 2023 00:55:58 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Fri, 16 Jun 2023 00:55:58 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Fri, 16 Jun 2023 00:55:58 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Fri, 16 Jun 2023 00:55:58 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 16 Jun 2023 00:55:58 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 16 Jun 2023 00:56:37 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:f0412dfb1aaea4892c13dab6f771bcd79641a4bdcb521ce881f5dcfc0df9a7a5`  
		Last Modified: Tue, 06 Jun 2023 09:20:27 GMT  
		Size: 28.6 MB (28580519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a44936ceb299069d361540aea2d1a48e75762ffa7f88d807e24620de51b36a`  
		Last Modified: Fri, 16 Jun 2023 01:20:21 GMT  
		Size: 22.3 MB (22272785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901cddafc58794e67393be72c53af7ec3f2e170dd4561727f9a8ccde077b932c`  
		Last Modified: Fri, 16 Jun 2023 01:20:30 GMT  
		Size: 82.9 MB (82915095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:focal-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:19fbf9a26db2bc80b22a3b2c256b1d015a85edba2ca796ee48693be5f926102e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128448304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefde5ad70c9169d70539acb435d1bd2beb818b11776921801dbd3a218604696`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:14:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Jul 2023 15:14:33 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Jul 2023 15:15:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:15:18 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 04 Jul 2023 15:15:18 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Tue, 04 Jul 2023 15:15:18 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Tue, 04 Jul 2023 15:15:19 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Tue, 04 Jul 2023 15:15:19 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Jul 2023 15:15:19 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Jul 2023 15:16:02 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147f42c747ab635b96804be9ccbb833c7b6ebf61f5182530e770574a8ce5eeae`  
		Last Modified: Tue, 04 Jul 2023 15:26:19 GMT  
		Size: 22.1 MB (22068629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2fb45d83759e431a62955d61cceb47118cf9f17d00363c7cc9664596f85f2f`  
		Last Modified: Tue, 04 Jul 2023 15:26:25 GMT  
		Size: 79.2 MB (79181345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
