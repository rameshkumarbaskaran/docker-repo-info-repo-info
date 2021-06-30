## `swift:focal`

```console
$ docker pull swift@sha256:e1d44fcf14bc4f386e0a54e7e10340ab20bc32606ea2169b5b72b196116aa851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:5133c05ab67dc4f129d52340906fc72d331cbc2743107e1db67e997043f8463e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.1 MB (644142689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d21dc3dbb6eee87e979aa849a2b577cda697a62f50868d59fa7439dd7707a6`
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
# Fri, 18 Jun 2021 03:31:43 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     gnupg2     libc6-dev     libcurl4     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 18 Jun 2021 03:31:44 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 18 Jun 2021 03:31:44 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Tue, 29 Jun 2021 22:49:49 GMT
ARG SWIFT_BRANCH=swift-5.4.2-release
# Tue, 29 Jun 2021 22:49:49 GMT
ARG SWIFT_VERSION=swift-5.4.2-RELEASE
# Tue, 29 Jun 2021 22:49:49 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 29 Jun 2021 22:49:49 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.4.2-release SWIFT_VERSION=swift-5.4.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 29 Jun 2021 22:51:39 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Tue, 29 Jun 2021 22:51:44 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2baf9d9d48c25b93e3b8f83f7afbf48fedd14b9d7a3faa4d02e9d626c20c29a0`  
		Last Modified: Fri, 18 Jun 2021 04:18:34 GMT  
		Size: 94.8 MB (94770104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b5640125a180dac51915e0e4609710e65b1e61417e7da823104a6b6e7c0aaf`  
		Last Modified: Tue, 29 Jun 2021 23:18:01 GMT  
		Size: 520.8 MB (520818893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
