## `swift:slim`

```console
$ docker pull swift@sha256:9a08644d8e70e1458696fb9e0e504991d57cbbb5aa2c02e5751c65f274c4de82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:4ac4d2e6dbd1c517b9bb5d4fb5c07a7177b76ecc49c024825099660f7c8487b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87453337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fac9a9bdbc3850efd156006de6f604a7ccc68d9b7f587644d953e604e16f117`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:51:00 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 03 Oct 2023 05:51:00 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 03 Oct 2023 05:53:16 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:53:16 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 03 Oct 2023 05:53:16 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 03 Oct 2023 05:53:17 GMT
ARG SWIFT_BRANCH=swift-5.9-release
# Tue, 03 Oct 2023 05:53:17 GMT
ARG SWIFT_VERSION=swift-5.9-RELEASE
# Tue, 03 Oct 2023 05:53:17 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 03 Oct 2023 05:53:17 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9-release SWIFT_VERSION=swift-5.9-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 03 Oct 2023 05:53:47 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e470ad3bac2a5ce94744ed26165cc2166c2eff3168e445e69bdf2b3af5fd62`  
		Last Modified: Tue, 03 Oct 2023 06:02:50 GMT  
		Size: 19.2 MB (19193552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f29fa0fb4c577eb53934bb15e4627769ff7adfc814646a60efe8557309ce4`  
		Last Modified: Tue, 03 Oct 2023 06:02:53 GMT  
		Size: 37.8 MB (37818916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c292845f0248f1889e047acd4e3768837a163eda7faed409737dfa5e93db708c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84768813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b681ae6ad9f5d6b269c2a64da019f1f3607fb64ea8f5704c96c770c6b032344`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 03:11:07 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 13 Oct 2023 03:11:07 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 13 Oct 2023 03:13:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 13 Oct 2023 03:13:37 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 13 Oct 2023 03:13:37 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 13 Oct 2023 03:13:37 GMT
ARG SWIFT_BRANCH=swift-5.9-release
# Fri, 13 Oct 2023 03:13:37 GMT
ARG SWIFT_VERSION=swift-5.9-RELEASE
# Fri, 13 Oct 2023 03:13:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 03:13:37 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9-release SWIFT_VERSION=swift-5.9-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 03:14:08 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cb0413ea4af52712a026c020a1edd0454ad243985a249db921e73e0d498d12`  
		Last Modified: Fri, 13 Oct 2023 03:27:15 GMT  
		Size: 19.1 MB (19087954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04c61a84734e67ea8e8bad5c418395865e02371ce4f901b79d46c117c4ce002`  
		Last Modified: Fri, 13 Oct 2023 03:27:16 GMT  
		Size: 37.3 MB (37288920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
