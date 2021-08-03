## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:395c5387bc7f046751260af99b6d120bd7d39be0f2d80760a49c22bbd49429aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:d70e933798bd9c4305bdc066972b37ee1393524a18a5cb19acbdd2b424c13986
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.7 MB (841738960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19ad08cd945ff8116c05611dd0b8442ed21bbbac9d02d662c9e708a6ab75907`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Aug 2021 23:19:37 GMT
ADD file:4cbe5850096b1ae39fe377dfe25245d1d635eafcbe0f58e1dc20e75716131cd3 in / 
# Mon, 02 Aug 2021 23:19:38 GMT
CMD ["/bin/bash"]
# Mon, 02 Aug 2021 23:38:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Mon, 02 Aug 2021 23:38:22 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 02 Aug 2021 23:38:51 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2   tar   tzdata   zlib-devel
# Mon, 02 Aug 2021 23:38:53 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Mon, 02 Aug 2021 23:38:53 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 02 Aug 2021 23:38:54 GMT
ARG SWIFT_BRANCH=swift-5.4.2-release
# Mon, 02 Aug 2021 23:38:54 GMT
ARG SWIFT_VERSION=swift-5.4.2-RELEASE
# Mon, 02 Aug 2021 23:38:54 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 02 Aug 2021 23:38:54 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.4.2-release SWIFT_VERSION=swift-5.4.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 02 Aug 2021 23:40:37 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Mon, 02 Aug 2021 23:40:43 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:d36ac8072fa22f99e1b8c66984e2fa09296890d37276e65dd4dc83503a3cf4c2`  
		Last Modified: Fri, 30 Jul 2021 16:48:36 GMT  
		Size: 62.0 MB (61965674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf43e58a820a3ab98fe49ae45b1114252ace08cafd9d2bc3e4948330bdebafe`  
		Last Modified: Mon, 02 Aug 2021 23:58:04 GMT  
		Size: 260.2 MB (260217852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbecd8a9684e3bb44fc29b3d7471ca48e181531ea1dd53194cddfa8297eb877`  
		Last Modified: Mon, 02 Aug 2021 23:58:45 GMT  
		Size: 519.6 MB (519555434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
