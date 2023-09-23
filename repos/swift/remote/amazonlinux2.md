## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:8f007d680cff00df06d70bc1b088af5c30b75460201dc990b1d8fd2e5099f5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:2f654679bd158ec30bcbb2f6589080395522fe08263dd622397cbd7bb1c7c049
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.7 MB (955716012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55ca1c5e5aebdaf7e5f598233bbc4344219554ea0700a5c223de2e5b67d47af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:25 GMT
COPY dir:a2da562c67b011c1b42effadc6ff06b6f82996c9f8d8c5778282cf441aac39a5 in / 
# Sat, 23 Sep 2023 00:20:25 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:06:26 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 23 Sep 2023 01:06:26 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 23 Sep 2023 01:07:11 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Sat, 23 Sep 2023 01:07:14 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 23 Sep 2023 01:07:14 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Sat, 23 Sep 2023 01:07:14 GMT
ARG SWIFT_BRANCH=swift-5.9-release
# Sat, 23 Sep 2023 01:07:14 GMT
ARG SWIFT_VERSION=swift-5.9-RELEASE
# Sat, 23 Sep 2023 01:07:14 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 23 Sep 2023 01:07:14 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9-release SWIFT_VERSION=swift-5.9-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 23 Sep 2023 01:07:58 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Sat, 23 Sep 2023 01:08:05 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:9aa850931a9d85a578215adaccd39361fe6ec5a8c81ead1837d4c5d43415b66b`  
		Last Modified: Mon, 18 Sep 2023 18:32:31 GMT  
		Size: 62.5 MB (62469678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9dc7dd1a10911a4d18e3c9bab2fae6264a38b2d02cd1325a02a1d14f19440c`  
		Last Modified: Sat, 23 Sep 2023 01:28:45 GMT  
		Size: 288.0 MB (287963066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becb90460d2b501e175d5b56773a704fed36486a8a28b6a6112a03a22d753bfc`  
		Last Modified: Sat, 23 Sep 2023 01:29:30 GMT  
		Size: 605.3 MB (605283068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f490f927ace75626f602174fab5d50f61cdfe29893a1b03a5cbfccb734bc656d`  
		Last Modified: Sat, 23 Sep 2023 01:28:06 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:7eb677ab8cc08c21633ae9b3940ca45a63fec5a2d3f65b1f83bcd3994c299705
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.9 MB (917906353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23f88465b2f3b4386407e110456ad0de2b5424501fed2ac25afbb7068f563c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:39:47 GMT
COPY dir:5885a696cc03fd82c0c021dd701725b8b1bc11902dc8789780147154a555ba2a in / 
# Sat, 23 Sep 2023 00:39:48 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:33:30 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 23 Sep 2023 01:33:30 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 23 Sep 2023 01:34:02 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Sat, 23 Sep 2023 01:34:08 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 23 Sep 2023 01:34:08 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Sat, 23 Sep 2023 01:34:08 GMT
ARG SWIFT_BRANCH=swift-5.9-release
# Sat, 23 Sep 2023 01:34:08 GMT
ARG SWIFT_VERSION=swift-5.9-RELEASE
# Sat, 23 Sep 2023 01:34:09 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 23 Sep 2023 01:34:09 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9-release SWIFT_VERSION=swift-5.9-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 23 Sep 2023 01:34:53 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Sat, 23 Sep 2023 01:35:06 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:0cd473df417d2282c9d0586281fb9293e3faf1fb6481fa584bac46295844f59e`  
		Last Modified: Mon, 18 Sep 2023 18:32:30 GMT  
		Size: 64.2 MB (64161861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee39839e31ec733052fbe410ba58726d5369249f469b849675241cb2a625c39`  
		Last Modified: Sat, 23 Sep 2023 01:42:40 GMT  
		Size: 254.5 MB (254537482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a873e10c203d4ef0a44a48c344d5b125dc3520ed31cc9ad843c79539a77feff`  
		Last Modified: Sat, 23 Sep 2023 01:43:15 GMT  
		Size: 599.2 MB (599206810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1ad0b209256a6258729b2753120c2b40db92530dfc27ff994826ba27a2612c`  
		Last Modified: Sat, 23 Sep 2023 01:42:14 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
