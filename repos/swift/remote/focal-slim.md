## `swift:focal-slim`

```console
$ docker pull swift@sha256:ad0e7bc530af764e11722ca245c1cc0de19ad990bebaee2aa2aebdc6dd0fd756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:4cd85487f2a015f71c35c57a142ed327a0dda6abc7e7c2965e69cb3ffcc4b2ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90337871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22861da27431189c6faebb53b477437dd1dd46295cb904bd3b7cbbf78cbd281c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 03:28:43 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 18 Jun 2021 03:28:43 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 18 Jun 2021 03:29:04 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 18 Jun 2021 03:29:05 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 18 Jun 2021 03:29:05 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Tue, 29 Jun 2021 22:47:53 GMT
ARG SWIFT_BRANCH=swift-5.4.2-release
# Tue, 29 Jun 2021 22:47:54 GMT
ARG SWIFT_VERSION=swift-5.4.2-RELEASE
# Tue, 29 Jun 2021 22:47:54 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 29 Jun 2021 22:47:55 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.4.2-release SWIFT_VERSION=swift-5.4.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 29 Jun 2021 22:49:40 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8455223fbd642d0a4287c7e473f335bc195c1a119017b92a5e972fbc01d8deba`  
		Last Modified: Fri, 18 Jun 2021 04:17:56 GMT  
		Size: 22.3 MB (22250690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacb5b71c493d44484fe2fec5a1a37ea9220401e852897050adfc00e2abd8ca9`  
		Last Modified: Tue, 29 Jun 2021 23:16:22 GMT  
		Size: 39.5 MB (39533489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
