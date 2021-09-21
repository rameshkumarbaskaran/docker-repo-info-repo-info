## `swift:bionic`

```console
$ docker pull swift@sha256:941e2366d049ea39c198d8d2b17bdaea24b718c136bcc579662a4087ef71aee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:bionic` - linux; amd64

```console
$ docker pull swift@sha256:819099bf2bd0412b6d1d43ef3304f67927add37cabe9b636c59242a1b9a53efa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.9 MB (743863935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c734f44b8b4fbb1137d8c27c9bef908c9c57422fd350f029b956ff4b3ca441`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 05:12:26 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Tue, 31 Aug 2021 05:12:26 GMT
LABEL Description=Docker Container for the Swift programming language
# Tue, 31 Aug 2021 05:14:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4     libxml2     libedit2     libsqlite3-0     libc6-dev     binutils     libgcc-5-dev     libstdc++-5-dev     zlib1g-dev     libpython3.6     tzdata     git     pkg-config     && rm -r /var/lib/apt/lists/*
# Tue, 31 Aug 2021 05:14:28 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 31 Aug 2021 05:14:28 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Tue, 21 Sep 2021 19:27:20 GMT
ARG SWIFT_BRANCH=swift-5.5-release
# Tue, 21 Sep 2021 19:27:20 GMT
ARG SWIFT_VERSION=swift-5.5-RELEASE
# Tue, 21 Sep 2021 19:27:20 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 21 Sep 2021 19:27:20 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.5-release SWIFT_VERSION=swift-5.5-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 21 Sep 2021 19:29:49 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Tue, 21 Sep 2021 19:29:54 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e76d16250a8f57d79710747137a242f611fee2834b1e442c917d91153604c77`  
		Last Modified: Tue, 31 Aug 2021 06:09:52 GMT  
		Size: 124.7 MB (124693120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfd04121e514b8201a7e61bb3f9d7450ca4ab78883c71f0a9e8b468cd4082e6`  
		Last Modified: Tue, 21 Sep 2021 20:01:05 GMT  
		Size: 592.5 MB (592462075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d8ba76fdc7167354b2fcb235f11d17fc86facfeaa7aef1b571aa59f0e1d5aa`  
		Last Modified: Tue, 21 Sep 2021 19:59:41 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
