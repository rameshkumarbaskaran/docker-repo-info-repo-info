## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:cdab6949428489ba034768003485dabd5149dadc0765fea4065a9a060d900e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:4c1d04d2ea49e7db6465bfeadf734faca9d209fd9c274d23062f43ac8f8c0243
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272569755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d112058d483f27f50272ae29e2575f17a58d94a5e3f80560db38ad80665b59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:37:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Thu, 09 Sep 2021 00:37:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 09 Sep 2021 00:39:43 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 09 Sep 2021 00:39:43 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 21 Sep 2021 19:41:51 GMT
ARG SWIFT_BRANCH=swift-5.5-release
# Tue, 21 Sep 2021 19:41:52 GMT
ARG SWIFT_VERSION=swift-5.5-RELEASE
# Tue, 21 Sep 2021 19:41:52 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 21 Sep 2021 19:41:52 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.5-release SWIFT_VERSION=swift-5.5-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 21 Sep 2021 19:43:35 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d1dad3aa3e7e240edd1d973052bd3a5c9241a67cc8e6357822399953009554`  
		Last Modified: Tue, 21 Sep 2021 20:09:40 GMT  
		Size: 210.6 MB (210569452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
