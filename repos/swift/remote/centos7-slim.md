## `swift:centos7-slim`

```console
$ docker pull swift@sha256:4acdf607a4fe425f7d4c4b466945d0497ef2322871f5864e0b912d035034e7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:centos7-slim` - linux; amd64

```console
$ docker pull swift@sha256:c92aa410e1be81a52fb0b2ff8f07ddb18435b5b060fbf1ad8a0a2f7772c89b36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108109818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7659ddfe286034be729ce6b329c193e34ca695a1a906f846c71edb40617e213f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 00:49:23 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Sat, 14 Nov 2020 00:49:23 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 14 Nov 2020 00:51:28 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 14 Nov 2020 00:51:28 GMT
ARG SWIFT_PLATFORM=centos7
# Sat, 14 Nov 2020 00:51:29 GMT
ARG SWIFT_BRANCH=swift-5.3-release
# Sat, 14 Nov 2020 00:51:29 GMT
ARG SWIFT_VERSION=swift-5.3-RELEASE
# Sat, 14 Nov 2020 00:51:29 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Sat, 14 Nov 2020 00:51:29 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=centos7 SWIFT_BRANCH=swift-5.3-release SWIFT_VERSION=swift-5.3-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Sat, 14 Nov 2020 00:52:31 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec31b4ebbfc97069c67d65a4ae3e8d845cc4c445e05502d855960ed0efbcf53b`  
		Last Modified: Sat, 14 Nov 2020 00:58:51 GMT  
		Size: 32.0 MB (32012661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
