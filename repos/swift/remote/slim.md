## `swift:slim`

```console
$ docker pull swift@sha256:4bc2e80cb8add0f5ff35c0b735156a2f6a34065d2e5d952812fc655860c4470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:23e53c8f047df01bf41a13e54a846bb70c44bf688e29fb71509b7d87019eccb7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86782643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb568ff4b405ae4e28dade7d72d6e76efcc18a3236065842508d6f60592cc59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 03:18:59 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 18 Jun 2021 03:19:00 GMT
LABEL Description=Docker Container for the Swift programming language
# Fri, 18 Jun 2021 03:25:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 18 Jun 2021 03:25:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 18 Jun 2021 03:25:32 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Tue, 29 Jun 2021 22:44:15 GMT
ARG SWIFT_BRANCH=swift-5.4.2-release
# Tue, 29 Jun 2021 22:44:15 GMT
ARG SWIFT_VERSION=swift-5.4.2-RELEASE
# Tue, 29 Jun 2021 22:44:16 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 29 Jun 2021 22:44:16 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.4.2-release SWIFT_VERSION=swift-5.4.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 29 Jun 2021 22:45:55 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21d83f2ecf2102730363f4a546c2014d9d9f46beb1fd8733bf6bb0091b89603`  
		Last Modified: Fri, 18 Jun 2021 04:17:09 GMT  
		Size: 20.5 MB (20493910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5eae737fd06b84f5d0b4bc2aa4da44ddba7fb3844024919203604fc4a633b`  
		Last Modified: Tue, 29 Jun 2021 23:15:37 GMT  
		Size: 39.6 MB (39588027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
