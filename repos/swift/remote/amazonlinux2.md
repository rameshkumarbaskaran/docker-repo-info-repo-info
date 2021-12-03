## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:e9e727307b710e79ea577e867e0afbf794c727ca571278e7179c7375766bc3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:b783ef6653ca04790ffc41af05ad9a7ac73d262a091b4173b1d67d89b813458b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.4 MB (920350829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88defadbfc544e2e2b4c7157cf80c1d1bd8049483fe868a4a9632dc3597c5854`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 23:20:03 GMT
ADD file:4eca58da351122eac20ffd87e3af2c0313089cb81650bdd4c2ef95a556fb842a in / 
# Thu, 02 Dec 2021 23:20:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Dec 2021 21:28:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 03 Dec 2021 21:28:07 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 03 Dec 2021 21:28:39 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2   tar   tzdata   zlib-devel
# Fri, 03 Dec 2021 21:28:41 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 03 Dec 2021 21:28:41 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 03 Dec 2021 21:28:41 GMT
ARG SWIFT_BRANCH=swift-5.5.1-release
# Fri, 03 Dec 2021 21:28:41 GMT
ARG SWIFT_VERSION=swift-5.5.1-RELEASE
# Fri, 03 Dec 2021 21:28:41 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 Dec 2021 21:28:42 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.5.1-release SWIFT_VERSION=swift-5.5.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 Dec 2021 21:29:39 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 03 Dec 2021 21:29:44 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:8b8a142162d22658bdf0283afcd00a9dd216c6637943ffe5f2ba53c4e3da0bd9`  
		Last Modified: Thu, 02 Dec 2021 06:01:08 GMT  
		Size: 62.1 MB (62090346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5ee3fcaebe508d85f808f9b961588955ef20079014f570ab21cba4a30d0f50`  
		Last Modified: Fri, 03 Dec 2021 21:43:52 GMT  
		Size: 267.2 MB (267209838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508a43f5ec6d91479c2dfe2c9d17a5f52461bad6612ac109e37ede644a190770`  
		Last Modified: Fri, 03 Dec 2021 21:44:43 GMT  
		Size: 591.1 MB (591050418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609d9b99a80b25777fc68ac4fb744a379fbbf412269a04f11b2e71e14f5e3782`  
		Last Modified: Fri, 03 Dec 2021 21:43:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
