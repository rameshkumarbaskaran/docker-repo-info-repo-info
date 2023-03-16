## `swift:latest`

```console
$ docker pull swift@sha256:1949f53ebe125353745499b8d155d1fff422b48164a482992420de4b8ec75db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:fe567a6fc37d3a3a88e461f7860956b8c3e49f28f27f914df595cdb3405e6c60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.8 MB (685764509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ff65b28f97dbda67570fca10ba1794b28c96c63d29fa543402b40ee6a88a8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:30:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 16 Mar 2023 01:30:10 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 16 Mar 2023 01:31:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:31:33 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 16 Mar 2023 01:31:33 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 16 Mar 2023 01:31:33 GMT
ARG SWIFT_BRANCH=swift-5.7.3-release
# Thu, 16 Mar 2023 01:31:33 GMT
ARG SWIFT_VERSION=swift-5.7.3-RELEASE
# Thu, 16 Mar 2023 01:31:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 16 Mar 2023 01:31:33 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7.3-release SWIFT_VERSION=swift-5.7.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 16 Mar 2023 01:32:07 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Thu, 16 Mar 2023 01:32:12 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19820ca64eeb9d53f801aba50e6ea5410045c1706aa8a3d02fbe76e6526f7308`  
		Last Modified: Thu, 16 Mar 2023 02:05:13 GMT  
		Size: 103.5 MB (103483113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bdd0b87410c42ce8ccc39921d3811172960a9c129f50c5440642d63dcd4e1f`  
		Last Modified: Thu, 16 Mar 2023 02:06:12 GMT  
		Size: 551.9 MB (551851206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05a65aaa943904c2a87c6a723612c303183e362a94933d663bab361b81270f7`  
		Last Modified: Thu, 16 Mar 2023 02:04:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:latest` - linux; arm64 variant v8

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
