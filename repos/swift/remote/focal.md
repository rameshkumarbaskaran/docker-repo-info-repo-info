## `swift:focal`

```console
$ docker pull swift@sha256:0c88438333f09297b72894ab018e6de3d1944912ee36e68c14949e9216669ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:a05a3bb82b1b34d13dee0f82a6f2f111cfa952b266a83d97ff205c3648f62048
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.0 MB (721965193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7dadf432bca93aa185de107526cd009b92dffa1362c1702eb9ca1ed3d28b9b`
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
# Wed, 02 Feb 2022 08:14:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     gnupg2     libc6-dev     libcurl4     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Wed, 02 Feb 2022 08:14:56 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 02 Feb 2022 08:14:57 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 02 Feb 2022 08:14:57 GMT
ARG SWIFT_BRANCH=swift-5.5.2-release
# Wed, 02 Feb 2022 08:14:57 GMT
ARG SWIFT_VERSION=swift-5.5.2-RELEASE
# Wed, 02 Feb 2022 08:14:57 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Feb 2022 08:14:57 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.5.2-release SWIFT_VERSION=swift-5.5.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Feb 2022 08:16:23 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Wed, 02 Feb 2022 08:16:26 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf9c9ea52ba39edfc38a2fc58c16c15e74c46e14a8c4d67491f862ec45226bd`  
		Last Modified: Wed, 02 Feb 2022 08:44:08 GMT  
		Size: 99.0 MB (99008891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7eb27ef6737f33bafdd665c571430a06ba449aee1115a5ef2f882128ab224b`  
		Last Modified: Wed, 02 Feb 2022 08:45:16 GMT  
		Size: 594.4 MB (594391976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bed3806de7244d80cca22909113e89d7ec91f79cfc2464f5106cbf2e2ead3d`  
		Last Modified: Wed, 02 Feb 2022 08:43:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
