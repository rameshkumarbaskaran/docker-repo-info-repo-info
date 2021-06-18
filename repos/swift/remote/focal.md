## `swift:focal`

```console
$ docker pull swift@sha256:f9095ae6e65fa9c22d942d0580f675dde406fa62b3ef5ed91eb95ee059634642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:ea8aa55c16f4eeff91b1abc59ea71edf38eed8e33ef35be1fe22c3f6da66ded4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.1 MB (644140537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee197f86c0057bf515f2552897ae587e6dfc23f9c8a54c60ba82d697393d4dab`
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
# Fri, 18 Jun 2021 03:31:44 GMT
ARG SWIFT_BRANCH=swift-5.4.1-release
# Fri, 18 Jun 2021 03:31:45 GMT
ARG SWIFT_VERSION=swift-5.4.1-RELEASE
# Fri, 18 Jun 2021 03:31:45 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 18 Jun 2021 03:31:45 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.4.1-release SWIFT_VERSION=swift-5.4.1-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 18 Jun 2021 03:33:16 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 18 Jun 2021 03:33:19 GMT
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
	-	`sha256:82758faadd28db5d13bb7ba21353e7f84315bad7d91b52d3f014bf4bc3842a52`  
		Last Modified: Fri, 18 Jun 2021 04:19:31 GMT  
		Size: 520.8 MB (520816741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
