## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:4777a28b9d87d96c4085b54d1d8ab3a4775a50da52fae909d7fea56baf9779f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:555fb508720b558de8bf21873c0b757e10d15d7e71c063d66ade11a5057cc612
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **863.1 MB (863141912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1563a6874ccfdae2e09b398d9c848f259f37aa5d662897a62f023520e48b040d`
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
# Fri, 22 Apr 2022 00:17:48 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 22 Apr 2022 00:17:50 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 22 Apr 2022 00:17:50 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 22 Apr 2022 00:17:50 GMT
ARG SWIFT_BRANCH=swift-5.6.1-release
# Fri, 22 Apr 2022 00:17:50 GMT
ARG SWIFT_VERSION=swift-5.6.1-RELEASE
# Fri, 22 Apr 2022 00:17:50 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 Apr 2022 00:17:50 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.6.1-release SWIFT_VERSION=swift-5.6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 Apr 2022 00:18:31 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 22 Apr 2022 00:18:37 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:ac1397dc8419bf1767b60a5cc5849b7130406030581d4542e48965801c303a70`  
		Last Modified: Thu, 21 Apr 2022 22:08:36 GMT  
		Size: 62.3 MB (62265199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef436ed41305c8636bc72e66849a3c50e6877102ec1f81f755e0740e9927df0`  
		Last Modified: Fri, 22 Apr 2022 00:50:54 GMT  
		Size: 275.9 MB (275916915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebe233c6a3233d076535a641e1973f35245054f4a80419d05d8cd1b9266c64e`  
		Last Modified: Fri, 22 Apr 2022 00:51:36 GMT  
		Size: 525.0 MB (524959572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06146644e3747576f19026fcbba4d007fd1b646f3ae33b1a7242dc397ff8b98`  
		Last Modified: Fri, 22 Apr 2022 00:50:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:e3fa5e9c233eb2968a7ca908c353bb22bec0aba19dc257d77e5eb4b6fe4c4888
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.1 MB (805071352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0669141b673a0c99d9a7500bc99eaf89fdad6ed178f8e8103768077fc1005ce3`
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
# Fri, 22 Apr 2022 02:42:54 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 22 Apr 2022 02:42:55 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 22 Apr 2022 02:42:56 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 22 Apr 2022 02:42:57 GMT
ARG SWIFT_BRANCH=swift-5.6.1-release
# Fri, 22 Apr 2022 02:42:58 GMT
ARG SWIFT_VERSION=swift-5.6.1-RELEASE
# Fri, 22 Apr 2022 02:42:59 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 Apr 2022 02:43:00 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.6.1-release SWIFT_VERSION=swift-5.6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 Apr 2022 02:43:33 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 22 Apr 2022 02:43:35 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:86bcd0b49e3391c117b5e27756fdf585aadc1a7b9054d19af0faa050839a6633`  
		Last Modified: Thu, 21 Apr 2022 22:59:02 GMT  
		Size: 63.9 MB (63888157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184f02ad1027f648d0419860aedd97dc7034fc244ea9717de49edf993a996d0`  
		Last Modified: Fri, 22 Apr 2022 02:47:10 GMT  
		Size: 236.0 MB (236013705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100cbc77c7c2ae0277f830d6b177332fa37a9fb96067f6d6939c4101883b4a6`  
		Last Modified: Mon, 11 Apr 2022 20:39:46 GMT  
		Size: 505.2 MB (505169287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b592f827ea6950454ed6bf4ffe974ac170c33d93db5c0a1b2c48d704c5e9e4f`  
		Last Modified: Fri, 22 Apr 2022 02:46:42 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
