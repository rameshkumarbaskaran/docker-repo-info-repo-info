## `swift:centos8`

```console
$ docker pull swift@sha256:57441b9438ca2178b4c7eb4a605852f2ac057d9a36c2f299bd68cf0dc2ba5495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:centos8` - linux; amd64

```console
$ docker pull swift@sha256:24767a8aaed153f6cadf5b2e458cda8d20eefdc68138a2e5f2d62450aadc4fbb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.4 MB (666446236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b2b6986c84f943dcc97910eab9d48bded4c17ef3ca7a49e1f0d1c29fa9f6a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Mon, 10 Aug 2020 18:54:53 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Mon, 10 Aug 2020 18:54:53 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 10 Aug 2020 18:54:58 GMT
RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm
# Tue, 11 Aug 2020 19:34:36 GMT
RUN yum install --enablerepo=PowerTools -y   binutils   gcc   git   glibc-static   libbsd-devel   libedit   libedit-devel   libicu-devel   libstdc++-static   pkg-config   python2   sqlite   zlib-devel
# Tue, 11 Aug 2020 19:34:37 GMT
RUN ln -s /usr/bin/python2 /usr/bin/python
# Tue, 11 Aug 2020 19:34:37 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 11 Aug 2020 19:34:37 GMT
ARG SWIFT_PLATFORM=centos8
# Mon, 16 Nov 2020 19:57:35 GMT
ARG SWIFT_BRANCH=swift-5.3.1-release
# Mon, 16 Nov 2020 19:57:35 GMT
ARG SWIFT_VERSION=swift-5.3.1-RELEASE
# Mon, 16 Nov 2020 19:57:35 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 16 Nov 2020 19:57:35 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=centos8 SWIFT_BRANCH=swift-5.3.1-release SWIFT_VERSION=swift-5.3.1-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 16 Nov 2020 19:58:48 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Mon, 16 Nov 2020 19:58:51 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be07b5b1fe3516caf3f86f7cb63b4f42d7e7cf71c8572a9dba481f027eb68e`  
		Last Modified: Mon, 10 Aug 2020 18:58:12 GMT  
		Size: 18.5 MB (18480138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2443fd6da2aa2fe7ae70de62ef128181a52f9a71db6dcb4cf480d732d50d8570`  
		Last Modified: Tue, 11 Aug 2020 19:49:14 GMT  
		Size: 147.7 MB (147666737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197c9c7edfa04f68b90e2cebe361edc2e2fe019ca693b09e2af8d50d19542f41`  
		Last Modified: Tue, 11 Aug 2020 19:48:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63ef3a6c74bb59e02311ac09f7209fc326ec4be05e7b7a041c8bc0619f82360`  
		Last Modified: Mon, 16 Nov 2020 20:13:13 GMT  
		Size: 425.4 MB (425431087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
