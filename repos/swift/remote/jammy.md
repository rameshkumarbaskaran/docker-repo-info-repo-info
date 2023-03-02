## `swift:jammy`

```console
$ docker pull swift@sha256:848df28530e7ff2f58e5c7d101e61a9a0f7ee62f43f36fcce823840853586361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:6c95a0eebb0cddfb929778e76040fbee99809c1cc6f46164a35d2d057c313be9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.8 MB (685758984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df1c304ff2cf05b69a28a38a4c3eea576031d322458865991b04d5a39cc31c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 21:19:17 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 31 Jan 2023 21:19:17 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 31 Jan 2023 21:21:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Tue, 31 Jan 2023 21:21:03 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 31 Jan 2023 21:21:03 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 31 Jan 2023 21:21:03 GMT
ARG SWIFT_BRANCH=swift-5.7.3-release
# Tue, 31 Jan 2023 21:21:03 GMT
ARG SWIFT_VERSION=swift-5.7.3-RELEASE
# Tue, 31 Jan 2023 21:21:03 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 31 Jan 2023 21:21:04 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7.3-release SWIFT_VERSION=swift-5.7.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 31 Jan 2023 21:21:46 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Tue, 31 Jan 2023 21:21:53 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:10ac4908093d4325f2c94b2c9a571fa1071a17a72dd9c21c1ffb2c86f68ca028`  
		Last Modified: Thu, 26 Jan 2023 08:46:26 GMT  
		Size: 30.4 MB (30429004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3635ef3e6c8709beb1a04f7e39b1a4135c2ddb14b245ea80a41b7536bd8ca194`  
		Last Modified: Tue, 31 Jan 2023 21:58:25 GMT  
		Size: 103.5 MB (103478738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e634e91ebb6ebfb17be7218e6426be25558eb303cbe7de79befac9c92feab9c`  
		Last Modified: Tue, 31 Jan 2023 21:59:26 GMT  
		Size: 551.9 MB (551851015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6a59ec41c52b3fe7549ddf1db9f33f2c01aadbb6feea3000718558c56462f1`  
		Last Modified: Tue, 31 Jan 2023 21:58:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c33c47468555ea68c89a5e4f81cc2f67b909ee8bc2b930776618d8cc28763111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.4 MB (671354255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e99fd188c58c5e0735d7cea4c9f6740f68501f6266d6c196dd2c704b64d006`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:47:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:48:01 GMT
ADD file:cf91de9ab30abab112d58c0a7f3bbb35853a02b2e406c65c89430ff049573c47 in / 
# Wed, 01 Mar 2023 04:48:01 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:14:27 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 02 Mar 2023 04:14:27 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 02 Mar 2023 04:15:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:15:01 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 02 Mar 2023 04:15:02 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 02 Mar 2023 04:15:02 GMT
ARG SWIFT_BRANCH=swift-5.7.3-release
# Thu, 02 Mar 2023 04:15:02 GMT
ARG SWIFT_VERSION=swift-5.7.3-RELEASE
# Thu, 02 Mar 2023 04:15:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 02 Mar 2023 04:15:02 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7.3-release SWIFT_VERSION=swift-5.7.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 02 Mar 2023 04:15:45 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Thu, 02 Mar 2023 04:15:57 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:986c4f6be3072d9528a459c780295bd053806536d2295a6de6aad327eaf19fad`  
		Last Modified: Wed, 01 Mar 2023 09:02:52 GMT  
		Size: 28.4 MB (28387922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e982df9eb5fb4205b355ef9c80c7dc08dcafa15cfcb56d3f4227880e15a10f`  
		Last Modified: Thu, 02 Mar 2023 04:22:51 GMT  
		Size: 100.7 MB (100670010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba8dd20ec29c196e3eb4c0a08de2ac85a2a1ac327b559e40eb9523db30fc494`  
		Last Modified: Thu, 02 Mar 2023 04:23:32 GMT  
		Size: 542.3 MB (542296095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa92c199fae8868cbc66cf882a170ef7d4e1604345a66f119c6dfa10af254256`  
		Last Modified: Thu, 02 Mar 2023 04:22:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
