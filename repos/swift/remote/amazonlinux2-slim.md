## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:5dc82d2475d12b62e77d4324a846fbf81a5479779b6566f31fa80fe7f59fa390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:4d002cbafd8b501099de139aae44c92524af5418290bc699e4edcdea9e396ea0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215535958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6d2a6727b2a2182d3ad151022db3231c5a62ed861a8c72e584f55491cf75fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Fri, 16 Jul 2021 00:06:52 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 16 Jul 2021 00:06:52 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 16 Jul 2021 00:09:02 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 16 Jul 2021 00:09:03 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 16 Jul 2021 00:09:03 GMT
ARG SWIFT_BRANCH=swift-5.4.2-release
# Fri, 16 Jul 2021 00:09:03 GMT
ARG SWIFT_VERSION=swift-5.4.2-RELEASE
# Fri, 16 Jul 2021 00:09:03 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 16 Jul 2021 00:09:03 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.4.2-release SWIFT_VERSION=swift-5.4.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 16 Jul 2021 00:10:28 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab22cce9199544c3dbb4eaceb82d0ff26a17352a3425ce10155d8ea1b3d0d8`  
		Last Modified: Fri, 16 Jul 2021 00:28:35 GMT  
		Size: 153.6 MB (153569952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
