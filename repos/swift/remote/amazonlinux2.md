## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:4d768fa413f7823ed8c79eb2d2bb2a1770f97e38e17815bb1b04f00493cc9a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:f7318ba210ce1afccc4a4b717e3f60bc7a1276be627159e35b6636a8b2f93a91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.3 MB (961337150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e3975d558a70543878a6f0bfe633547613e993a312a921c4234eb6479485b9`
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
# Wed, 25 Oct 2023 02:02:26 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Wed, 25 Oct 2023 02:02:28 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 25 Oct 2023 02:02:28 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 25 Oct 2023 02:02:28 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Wed, 25 Oct 2023 02:02:28 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Wed, 25 Oct 2023 02:02:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Oct 2023 02:02:28 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Oct 2023 02:03:18 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 25 Oct 2023 02:03:24 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:e6a2a106da1df9b5d4bfa74686415ac760f9d9999604e3784820d596e0983e27`  
		Last Modified: Wed, 25 Oct 2023 01:11:13 GMT  
		Size: 62.5 MB (62492148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a63d3eb129128f9edf712e62d4a566d112e92a5852d0760a9af557f9b83d0`  
		Last Modified: Wed, 25 Oct 2023 02:20:56 GMT  
		Size: 290.6 MB (290583050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc22a1dcedd7a2b0ee5355b448253e2606780634d79da288e117b0717b5d342`  
		Last Modified: Wed, 25 Oct 2023 02:21:44 GMT  
		Size: 608.3 MB (608261753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b860ef23bd5106830b46610431fddd39deb0a0f7ae5f99857e73c1ebb72c9471`  
		Last Modified: Wed, 25 Oct 2023 02:20:22 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:5bb16b46ebb767d324e9ccb83326a15a67a56fbecde5e90f3aece902034f4001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.2 MB (923193711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17b3625831cfb80f1f35f074ddbb6cd27ddd89c188a9df0c964fcc9472b6fe6`
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
# Wed, 25 Oct 2023 01:04:19 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Wed, 25 Oct 2023 01:04:24 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 25 Oct 2023 01:04:24 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 25 Oct 2023 01:04:24 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Wed, 25 Oct 2023 01:04:24 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Wed, 25 Oct 2023 01:04:24 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Oct 2023 01:04:24 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Oct 2023 01:05:07 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 25 Oct 2023 01:05:20 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:bceed9d4335ecd25da3cee660b39ab03c762b3e6bc197470f6eeeaad4c7f3db4`  
		Last Modified: Wed, 25 Oct 2023 00:40:19 GMT  
		Size: 64.2 MB (64228438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54eb1971e6132e81d4dbf1145c8a6166a25d6ba958ca728d5c6b44bfdf02576`  
		Last Modified: Wed, 25 Oct 2023 01:11:58 GMT  
		Size: 256.9 MB (256884204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f096a389a50b03794c7704b40460cc74a86ca0bb33630b85b1c5f9434286d98c`  
		Last Modified: Wed, 25 Oct 2023 01:12:33 GMT  
		Size: 602.1 MB (602080870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56afa6f4ee36d3d17a0966e8f779bb5ab33983333f9b2fdeb82ef305dead2eb`  
		Last Modified: Wed, 25 Oct 2023 01:11:32 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
