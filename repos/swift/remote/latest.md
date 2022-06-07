## `swift:latest`

```console
$ docker pull swift@sha256:8ceb840c7efcb24ac94539d4f10b285d380ae34493672c965ab393a246ff6692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:2a5700d472d753a62aea50ab7dfb64614237f983a75f6492da5d59ecdd7d8568
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.6 MB (704557537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4c42bdf4453fc7ac9c8b214d68d11fd6bfa4535ff6039b72cfad39a6fc365a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 03:18:23 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 07 Jun 2022 03:18:23 GMT
LABEL Description=Docker Container for the Swift programming language
# Tue, 07 Jun 2022 03:19:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4-openssl-dev     libxml2-dev     libedit2     libsqlite3-0     libc6-dev     binutils     libgcc-5-dev     libstdc++-5-dev     zlib1g-dev     libpython3.6     tzdata     git     pkg-config     && rm -r /var/lib/apt/lists/*
# Tue, 07 Jun 2022 03:19:25 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 07 Jun 2022 03:19:25 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Tue, 07 Jun 2022 03:19:25 GMT
ARG SWIFT_BRANCH=swift-5.6.1-release
# Tue, 07 Jun 2022 03:19:25 GMT
ARG SWIFT_VERSION=swift-5.6.1-RELEASE
# Tue, 07 Jun 2022 03:19:25 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Jun 2022 03:19:25 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.6.1-release SWIFT_VERSION=swift-5.6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Jun 2022 03:20:03 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Tue, 07 Jun 2022 03:20:09 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ee073ea97359fa18f28b942357e5af51455ec82460ceb3a2d006995b267369`  
		Last Modified: Tue, 07 Jun 2022 03:44:39 GMT  
		Size: 151.7 MB (151738050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa69c35f83054c59c19ba56bcb11d46e0fbd2ecd9d1ad789115ba87a91d48015`  
		Last Modified: Tue, 07 Jun 2022 03:45:29 GMT  
		Size: 526.1 MB (526107633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1d26b0539369fec0fbeb841d8129aeab8dea1db63d7fbfe072f3ad93510e54`  
		Last Modified: Tue, 07 Jun 2022 03:44:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
