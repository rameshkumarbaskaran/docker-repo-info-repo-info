## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:2d9151ad0527c50b5ae0baa48584ea2dddb1f0c4cfac49635effd5b7962577b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:171c294303129557089ea46a32cb486cdb2968eef1157d0bb6a2b8fbfa26563f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200300113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8789d64872a2bdaa006a5837ae2b4a2dedc9a057e1bbe2145dc7e6c36ad97415`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 24 Feb 2021 19:19:48 GMT
ADD file:40bc6ac9b95149d9077e8e692feea2208fcd1c5883673953b295e6acd014ea38 in / 
# Wed, 24 Feb 2021 19:19:48 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:01:50 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 26 Mar 2021 14:01:50 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 26 Mar 2021 14:03:46 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 26 Mar 2021 14:03:46 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 26 Mar 2021 14:03:47 GMT
ARG SWIFT_BRANCH=swift-5.3.3-release
# Fri, 26 Mar 2021 14:03:47 GMT
ARG SWIFT_VERSION=swift-5.3.3-RELEASE
# Fri, 26 Mar 2021 14:03:47 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 26 Mar 2021 14:03:47 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.3.3-release SWIFT_VERSION=swift-5.3.3-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 26 Mar 2021 14:04:56 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:9da98c321efd693e1dc19cc24c7c2cfa365c649f178da8ebdfdc5243d0b2f91a`  
		Last Modified: Wed, 24 Feb 2021 10:37:31 GMT  
		Size: 61.9 MB (61935160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d569d1ed8b3b25953b741f6ae10e6d8103740c09c6b3e5d982ffda9fd671c74e`  
		Last Modified: Fri, 26 Mar 2021 14:54:47 GMT  
		Size: 138.4 MB (138364953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
