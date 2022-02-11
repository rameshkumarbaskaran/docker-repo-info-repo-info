## `swift:bionic-slim`

```console
$ docker pull swift@sha256:4eead5d10a27bc5e0f2e29ff0a11e443b9e7ba72975d1e28b8db5c94ebe1dc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:bionic-slim` - linux; amd64

```console
$ docker pull swift@sha256:290ca79668e6254812042b4704d062c91673a827fda91a825a2c24d1238af614
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139939423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d3dd0de4483d40cc5b75b92de4df16d8aca6d323f9e075e2792bf546b1a4ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 08:07:39 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 02 Feb 2022 08:07:39 GMT
LABEL Description=Docker Container for the Swift programming language
# Wed, 02 Feb 2022 08:11:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Wed, 02 Feb 2022 08:11:00 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 02 Feb 2022 08:11:00 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Fri, 11 Feb 2022 18:30:07 GMT
ARG SWIFT_BRANCH=swift-5.5.3-release
# Fri, 11 Feb 2022 18:30:07 GMT
ARG SWIFT_VERSION=swift-5.5.3-RELEASE
# Fri, 11 Feb 2022 18:30:07 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 11 Feb 2022 18:30:07 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.5.3-release SWIFT_VERSION=swift-5.5.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 11 Feb 2022 18:31:28 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181c32681a078877744ee56d498cdf57dd874b2c400b7377f8bdbd1c9fbc11c6`  
		Last Modified: Wed, 02 Feb 2022 08:42:47 GMT  
		Size: 20.5 MB (20491206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dac53fa0725f1238d795cbb994d87bfe357750edc1a42fa2d4c191f26b6d461`  
		Last Modified: Fri, 11 Feb 2022 18:53:13 GMT  
		Size: 92.7 MB (92740151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
