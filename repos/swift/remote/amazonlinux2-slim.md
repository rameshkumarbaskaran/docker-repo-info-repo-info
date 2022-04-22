## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:fb8cb12c47a10dcf55cbd43fa5d0c5f5e7a897a119dae11dec3446bd8dd3a884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:111e0c524eef868f4183feeae2f529967b6e7f4572ac2d5fabbc7269e549ba7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274849703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526191593977bda015a9591e80c4067b7db7054218b9e1a17c2756b77894096c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:19:57 GMT
ADD file:4eb88d9d977dadb40c630d693a07ca066069b30b9751b7a421dfb4ba0b99d862 in / 
# Thu, 21 Apr 2022 22:19:58 GMT
CMD ["/bin/bash"]
# Fri, 22 Apr 2022 00:17:16 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 22 Apr 2022 00:17:16 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 22 Apr 2022 00:18:40 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 22 Apr 2022 00:18:40 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 22 Apr 2022 00:18:40 GMT
ARG SWIFT_BRANCH=swift-5.6.1-release
# Fri, 22 Apr 2022 00:18:40 GMT
ARG SWIFT_VERSION=swift-5.6.1-RELEASE
# Fri, 22 Apr 2022 00:18:40 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 Apr 2022 00:18:40 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.6.1-release SWIFT_VERSION=swift-5.6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 Apr 2022 00:19:13 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:ac1397dc8419bf1767b60a5cc5849b7130406030581d4542e48965801c303a70`  
		Last Modified: Thu, 21 Apr 2022 22:08:36 GMT  
		Size: 62.3 MB (62265199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7735b96721558f10f9fe92aab16de2715fab87e9ebef3a893967c18655f1842f`  
		Last Modified: Fri, 22 Apr 2022 00:52:11 GMT  
		Size: 212.6 MB (212584504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f69f4fa437e583b1ff41dd8286928e477775f8a592bd67a0da36a5b4a4bd26d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239481228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1582291e173fc87822199adf002cb9fa62a00a490105fdfd1408b17b0cdee0db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:57:49 GMT
ADD file:76e1ee72575f50a75573a46483631e239d3b6afda9fdd53086883bd03db5364b in / 
# Thu, 21 Apr 2022 22:57:51 GMT
CMD ["/bin/bash"]
# Fri, 22 Apr 2022 02:42:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 22 Apr 2022 02:42:32 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 22 Apr 2022 02:43:44 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 22 Apr 2022 02:43:45 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 22 Apr 2022 02:43:46 GMT
ARG SWIFT_BRANCH=swift-5.6.1-release
# Fri, 22 Apr 2022 02:43:47 GMT
ARG SWIFT_VERSION=swift-5.6.1-RELEASE
# Fri, 22 Apr 2022 02:43:48 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 Apr 2022 02:43:49 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.6.1-release SWIFT_VERSION=swift-5.6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 Apr 2022 02:44:20 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:86bcd0b49e3391c117b5e27756fdf585aadc1a7b9054d19af0faa050839a6633`  
		Last Modified: Thu, 21 Apr 2022 22:59:02 GMT  
		Size: 63.9 MB (63888157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2cddb3c76aa5b580f0a3dde9e2fc02a4c420361f98b899b2371a29368cccd0`  
		Last Modified: Fri, 22 Apr 2022 02:47:44 GMT  
		Size: 175.6 MB (175593071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
