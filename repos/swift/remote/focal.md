## `swift:focal`

```console
$ docker pull swift@sha256:9990ed155ee2406d61651face0b5cf22026df8b2e8a7c813aa3ae00d765de654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:5ee91fb3e155d8eba8ac144a243ec0ffcfc03f9a16f5d1d0efb5494f83a7e8e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **739.5 MB (739460635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced8c05267f21c19e1a00349557db7066f8ca7faecad2a42fc516fababd7c745`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 08:12:14 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 02 Feb 2022 08:12:15 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 11 Feb 2022 18:36:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 11 Feb 2022 18:36:09 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 11 Feb 2022 18:36:10 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Fri, 11 Feb 2022 18:36:10 GMT
ARG SWIFT_BRANCH=swift-5.5.3-release
# Fri, 11 Feb 2022 18:36:10 GMT
ARG SWIFT_VERSION=swift-5.5.3-RELEASE
# Fri, 11 Feb 2022 18:36:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 11 Feb 2022 18:36:10 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.5.3-release SWIFT_VERSION=swift-5.5.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 11 Feb 2022 18:37:25 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 11 Feb 2022 18:37:30 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361dfaba449950166b89f64f6ea35536ed2196631dbbd2c53796f230d8750548`  
		Last Modified: Fri, 11 Feb 2022 18:54:47 GMT  
		Size: 116.5 MB (116494821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ca34cf696a925b2372f66c0466b0285076370e006bc82a67f431018f787c3d`  
		Last Modified: Fri, 11 Feb 2022 18:55:53 GMT  
		Size: 594.4 MB (594401486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734b27be096b99d04e1844464cd30b3e5f2e754dc91d81c0d205f9100b8f5bc8`  
		Last Modified: Fri, 11 Feb 2022 18:54:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
