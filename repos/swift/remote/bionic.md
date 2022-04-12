## `swift:bionic`

```console
$ docker pull swift@sha256:82eab1e4ca7f883d3fd7612b9ea0199bc88a83fa091a3290a3b1f06bad7e157b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:bionic` - linux; amd64

```console
$ docker pull swift@sha256:317ba8eb06e645277604a686705fe3a5b297ba7d9d395e76d8d5f5696a8d0c04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.5 MB (704533698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4b5804093ba1f5d1c33e487c1bfdb537fe2b6c52293d8750b263673ab2aa1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:19:43 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 06 Apr 2022 03:19:43 GMT
LABEL Description=Docker Container for the Swift programming language
# Wed, 06 Apr 2022 03:21:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4-openssl-dev     libxml2-dev     libedit2     libsqlite3-0     libc6-dev     binutils     libgcc-5-dev     libstdc++-5-dev     zlib1g-dev     libpython3.6     tzdata     git     pkg-config     && rm -r /var/lib/apt/lists/*
# Wed, 06 Apr 2022 03:21:02 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 06 Apr 2022 03:21:02 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Mon, 11 Apr 2022 19:37:01 GMT
ARG SWIFT_BRANCH=swift-5.6.1-release
# Mon, 11 Apr 2022 19:37:01 GMT
ARG SWIFT_VERSION=swift-5.6.1-RELEASE
# Mon, 11 Apr 2022 19:37:01 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 11 Apr 2022 19:37:01 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.6.1-release SWIFT_VERSION=swift-5.6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 11 Apr 2022 19:37:42 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Mon, 11 Apr 2022 19:37:48 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc128aef939e12f63c51bc3d1340c2dc58d555523914a5005257693f1c4edf13`  
		Last Modified: Wed, 06 Apr 2022 03:47:13 GMT  
		Size: 151.7 MB (151717217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006cb2412769617de357c6cf017064bb0dc6c943b9491c2e7e2b42f62aa17abe`  
		Last Modified: Mon, 11 Apr 2022 19:52:45 GMT  
		Size: 526.1 MB (526107317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe2e640b8c3dc9bdc2777db4ddaeb963a6ee29e498f17058417895878a4630f`  
		Last Modified: Mon, 11 Apr 2022 19:51:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
