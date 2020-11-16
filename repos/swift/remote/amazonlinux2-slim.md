## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:33f856238f7cb2b6459ed4e7e7d4d9b0b21ace364cb5af1eeb677b884b65b7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:6d3f2957a0d7eeccf879b8713a8e0ff0fff21d0ec04669874c8b27fc37de98a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191834896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289770c60b292f11e3bd9c91aa7a10a0b02ce1aa1102647c6c7b7d479f24948f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 22:36:52 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 31 Jul 2020 22:36:52 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 11 Aug 2020 19:32:36 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 11 Aug 2020 19:32:37 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 16 Nov 2020 19:56:04 GMT
ARG SWIFT_BRANCH=swift-5.3.1-release
# Mon, 16 Nov 2020 19:56:04 GMT
ARG SWIFT_VERSION=swift-5.3.1-RELEASE
# Mon, 16 Nov 2020 19:56:04 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 16 Nov 2020 19:56:05 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.3.1-release SWIFT_VERSION=swift-5.3.1-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 16 Nov 2020 19:57:20 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db0eb1e1fdea2c267288567f3590baf1de5ad4f6fd8cd2c4e8275bf9fedf7ab`  
		Last Modified: Mon, 16 Nov 2020 20:11:53 GMT  
		Size: 130.1 MB (130118356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
