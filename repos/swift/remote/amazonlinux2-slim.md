## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:2cbcae9e2f59748a4a9ad9ce8f4a3ab4a2918c448ba15a73fc34dc0a118645dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:869e92c54bdf2a7d902c00eaec6da906ae8e4346747f26f9447f7f51166e078e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279625145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8873c43f8b5b134c9c25b5d3a79f78edbd3359381cff4136d530749a50220717`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Feb 2022 23:40:28 GMT
ADD file:871c80292a1347a65a30c9d2cd343d927528a61b8d89fd82f268d5f8ad4d2944 in / 
# Fri, 04 Feb 2022 23:40:29 GMT
CMD ["/bin/bash"]
# Sat, 05 Feb 2022 06:37:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 05 Feb 2022 06:37:42 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 05 Feb 2022 06:39:49 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 05 Feb 2022 06:39:49 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 11 Feb 2022 18:39:47 GMT
ARG SWIFT_BRANCH=swift-5.5.3-release
# Fri, 11 Feb 2022 18:39:47 GMT
ARG SWIFT_VERSION=swift-5.5.3-RELEASE
# Fri, 11 Feb 2022 18:39:47 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 11 Feb 2022 18:39:47 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.5.3-release SWIFT_VERSION=swift-5.5.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 11 Feb 2022 18:41:09 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:f964900200fc1f8473ac70d9da14cde8bae251ffb4a8f4792e2bf9baf6aaac70`  
		Last Modified: Thu, 27 Jan 2022 23:12:55 GMT  
		Size: 62.2 MB (62237845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cac32bf12f35f974199b25e5b3705551d0885cfbdcbbb42abbb1b1c817844`  
		Last Modified: Fri, 11 Feb 2022 18:58:13 GMT  
		Size: 217.4 MB (217387300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
