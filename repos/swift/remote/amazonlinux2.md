## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:9963a1a9893927ddbb69810bf98cd2805251315f8b3d97f065b2b332497220bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:6546bcbfd69068ad3e8f22998fa186372dcea0890d1b75895eac0ccc6abec45f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702916819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee272321cb22a01cd210ee01e94f05c72989958c7ad8aaba62f56fdccbd18360`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Apr 2020 18:22:56 GMT
ADD file:c64a7d77d1e9f4364c8d2009059cb8668697d61f54f457215b6be6f0c9cded5b in / 
# Tue, 21 Apr 2020 18:22:56 GMT
CMD ["/bin/bash"]
# Fri, 05 Jun 2020 01:42:50 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 05 Jun 2020 01:42:50 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 05 Jun 2020 01:45:18 GMT
RUN yum -y update && yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2   tar   tzdata   zlib-devel
# Fri, 05 Jun 2020 01:45:19 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 05 Jun 2020 01:45:19 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 05 Jun 2020 01:45:19 GMT
ARG SWIFT_BRANCH=swift-5.2.4-release
# Fri, 05 Jun 2020 01:45:19 GMT
ARG SWIFT_VERSION=swift-5.2.4-RELEASE
# Fri, 05 Jun 2020 01:45:19 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 05 Jun 2020 01:45:20 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.2.4-release SWIFT_VERSION=swift-5.2.4-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 05 Jun 2020 01:46:36 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 05 Jun 2020 01:46:38 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:a3f8e652bdc470bbea38766fe41f8f12b9e4d44e9ce4037eb502839754b06b9c`  
		Last Modified: Tue, 21 Apr 2020 18:23:48 GMT  
		Size: 61.6 MB (61619066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a964324294e4506013a9be63ac1ed10206f3b02f52621d4286b7f11bb1174c`  
		Last Modified: Fri, 05 Jun 2020 01:56:28 GMT  
		Size: 252.3 MB (252327798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c08d78a83c1cd45bff0c822a4760bdfeab10b2c0556eb5809fcd712c53043f9`  
		Last Modified: Fri, 05 Jun 2020 01:56:51 GMT  
		Size: 389.0 MB (388969955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
