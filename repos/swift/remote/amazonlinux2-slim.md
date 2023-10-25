## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:24b198cff8dcf70fb4c8f6fdf353b4b08c8869b32ccaea5798a96600c69bb2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:82d9c05a87e07391de8141cbfdb659734f67e4d9fcd216a80c2a7bf8a6e1738b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243064356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43702571e29cae27b89fafdebf5f7d9ea827432acda66fdd2ee55377627bd903`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Oct 2023 01:19:53 GMT
COPY dir:fdcfaddab7ba123e1840e939ec5f9c668c54d167449dc297fea5669f294f7222 in / 
# Wed, 25 Oct 2023 01:19:54 GMT
CMD ["/bin/bash"]
# Wed, 25 Oct 2023 02:01:56 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Oct 2023 02:01:56 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Oct 2023 02:03:34 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 25 Oct 2023 02:03:35 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 25 Oct 2023 02:03:35 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Wed, 25 Oct 2023 02:03:35 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Wed, 25 Oct 2023 02:03:35 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Oct 2023 02:03:35 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Oct 2023 02:04:13 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:e6a2a106da1df9b5d4bfa74686415ac760f9d9999604e3784820d596e0983e27`  
		Last Modified: Wed, 25 Oct 2023 01:11:13 GMT  
		Size: 62.5 MB (62492148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac7d4e3c51e548b65aae7c9f3ef8f5132c24c494e40db0b1caa1de499f2fbaa`  
		Last Modified: Wed, 25 Oct 2023 02:22:14 GMT  
		Size: 180.6 MB (180572208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:761682a53208471d8001bd95fca840927780a76ee69ca6c68352ee9d643d2cde
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215124082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3747200335825a8eaa1a780e6ba14441229c28024cc3f87bb342b13d4679d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Oct 2023 00:39:44 GMT
COPY dir:8cce6e6a6abbbd299b12dd9d8f9974415975c25f4170a182c4d6addd8ba9d101 in / 
# Wed, 25 Oct 2023 00:39:45 GMT
CMD ["/bin/bash"]
# Wed, 25 Oct 2023 01:03:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Oct 2023 01:03:56 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Oct 2023 01:05:33 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 25 Oct 2023 01:05:33 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 25 Oct 2023 01:05:33 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Wed, 25 Oct 2023 01:05:33 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Wed, 25 Oct 2023 01:05:34 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Oct 2023 01:05:34 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Oct 2023 01:06:06 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:bceed9d4335ecd25da3cee660b39ab03c762b3e6bc197470f6eeeaad4c7f3db4`  
		Last Modified: Wed, 25 Oct 2023 00:40:19 GMT  
		Size: 64.2 MB (64228438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7acb71b82e999e180fa8a9e76443deb07bb0cd0175a681bb3e7db50b8e6a973`  
		Last Modified: Wed, 25 Oct 2023 01:13:02 GMT  
		Size: 150.9 MB (150895644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
