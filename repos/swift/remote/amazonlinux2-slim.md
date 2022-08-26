## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:c0f2af7e9ef7f8463f918161f3c0ca2722f752e90c477f8ce9346f6a0ad9f0a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:6d2e416f71d8d0d98f2973da79e3d643fbb8a53a69cfb6e14ffd75dc41da29c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280269067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa535e316776426543f9459b819d9799c225f0b4ae6a7fb286679cf1bece065`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 03:06:36 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Aug 2022 03:06:36 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Aug 2022 03:08:14 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 12 Aug 2022 03:08:14 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 12 Aug 2022 03:08:15 GMT
ARG SWIFT_BRANCH=swift-5.6.2-release
# Fri, 12 Aug 2022 03:08:15 GMT
ARG SWIFT_VERSION=swift-5.6.2-RELEASE
# Fri, 12 Aug 2022 03:08:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Aug 2022 03:08:15 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.6.2-release SWIFT_VERSION=swift-5.6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Aug 2022 03:08:51 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef1c35086bbd99826c6cfb60312fe2fc19b4a350277c17d37c39377917173e9`  
		Last Modified: Fri, 12 Aug 2022 03:24:57 GMT  
		Size: 218.0 MB (217952851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:30d30a6b395cb28e61a0715ff9ac7be4d9cb65aff458d11061cb865b5735468d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245765977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d43ccf765edb1176cae3da7542184bea468e49b952d28bcf7f0376d1982062`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 00:56:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 26 Aug 2022 00:56:56 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 26 Aug 2022 00:58:21 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 26 Aug 2022 00:58:22 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 26 Aug 2022 00:58:23 GMT
ARG SWIFT_BRANCH=swift-5.6.2-release
# Fri, 26 Aug 2022 00:58:24 GMT
ARG SWIFT_VERSION=swift-5.6.2-RELEASE
# Fri, 26 Aug 2022 00:58:25 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 26 Aug 2022 00:58:26 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.6.2-release SWIFT_VERSION=swift-5.6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 26 Aug 2022 00:59:00 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea30dc92097756a3ea3c76c2911fd2d9cc23411ef4b74f9b24232a220f96d77`  
		Last Modified: Fri, 26 Aug 2022 01:00:40 GMT  
		Size: 181.8 MB (181827212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
