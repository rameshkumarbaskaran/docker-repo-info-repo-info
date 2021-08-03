## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:5d922b1de334717785be77a4bdcbd171c85af4d4ed8cae72a984aea8026d8d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:1e4145366a298023ae30b4feb102d05088b310cff9854fbee2ddcb3b60e97eb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216420444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebab803a403ab91ecebe827cd62300537f8197208ada56f8182004dc7845443`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Aug 2021 23:19:37 GMT
ADD file:4cbe5850096b1ae39fe377dfe25245d1d635eafcbe0f58e1dc20e75716131cd3 in / 
# Mon, 02 Aug 2021 23:19:38 GMT
CMD ["/bin/bash"]
# Mon, 02 Aug 2021 23:38:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Mon, 02 Aug 2021 23:38:22 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 02 Aug 2021 23:40:48 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Mon, 02 Aug 2021 23:40:48 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 02 Aug 2021 23:40:49 GMT
ARG SWIFT_BRANCH=swift-5.4.2-release
# Mon, 02 Aug 2021 23:40:49 GMT
ARG SWIFT_VERSION=swift-5.4.2-RELEASE
# Mon, 02 Aug 2021 23:40:49 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 02 Aug 2021 23:40:49 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.4.2-release SWIFT_VERSION=swift-5.4.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 02 Aug 2021 23:42:22 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:d36ac8072fa22f99e1b8c66984e2fa09296890d37276e65dd4dc83503a3cf4c2`  
		Last Modified: Fri, 30 Jul 2021 16:48:36 GMT  
		Size: 62.0 MB (61965674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb796c662b850527fe5053c29e2ee7745204a284910987e8168d7366698ed25`  
		Last Modified: Mon, 02 Aug 2021 23:59:16 GMT  
		Size: 154.5 MB (154454770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
